+++
title = "Datastructures on Hypercore - Queue"
date = 2023-12-01
+++

In the [previous post](../datastructures-on-hypercore-stack) we saw how we can
implement a stack on a hypercore. In this post I explore how to implement a queue
which turned out to be in some ways, more complex than a stack and also simpler.

## Take 1

**Enqueue and dequeue**

Enqeue adds a new element to the back of the queue which we can do by appending
a new block to the hypercore.

To perform a dequeue we need to find the front of
the queue, which is the first block, before we have done any dequeue operation.
But the front keeps increasing
as we perform more dequeues. So to find the front in O(1) time, we add a pointer
to it along with the new element during the append.

To record the new position during dequeue, we append a special block
with just the pointer to the front. Do distinguish the dequeue block, we show
X where the element used to be for an enqueue block.

You can see the hypercore state after 2 enqueues and a dequeue below.

![Queue on Hypercore - Take 1 - Step 3](hypercore-queue-1-3.excalidraw.png)


**Series of dequeues**

This system looks good till now, but is still not O(1) for the dequeue operation as
the blocks recording the dequeue states need to be skipped to find the new front.
This can be seen below where in step 7, when we do the dequeue operation, we need to 
skip blocks 5 and 6 before we find the new front, which is 7, and record it.

![Queue on Hypercore - Take 1 - Long series of deqeues](hypercore-queue-1-long-dequeue.excalidraw.png)


## Take 2

A simple solution for avoiding the clutter of the front pointers is to store it in
a different hypercore than where the elements of the queue is stored.
This is shown below

![Queue on Hypercore - Take 2](hypercore-queue-2-3.excalidraw.png)

We update the front of the hypercoreo only in case of a dequeue operation.

Now that is simple!