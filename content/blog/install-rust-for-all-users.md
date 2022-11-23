+++
title = "Install Rust for all users"
date = 2022-11-22
+++

So, I wanted a single rust compiler to be installed system wide, but the
default result of using [rustup](https://rustup.rs/) is, it is installed
locally in the current user's home directory.

After a bit of searching on the Internet and some dead ends, I stumbled on
<https://github.com/rust-lang/rustup/issues/1085> which seems to be mostly working.

Interesting thing I learned from the above is that, the script that was
suggested for 'rustc' can simply be symlinked to other commands like 'cargo'
and it still works as it uses some
[parameter expansion](http://mywiki.wooledge.org/BashSheet#Parameter_Operations)
magic.

Also for whatever reason I had to do a ```sudo rustup component add rust-src```
to make rust-analyzer work with Visual Studio Code.
