+++
title = "Access raw.githubusercontent.com files in India"
date = 2023-01-18
updated = 2023-09-05
+++

As of January 2023, raw.githubusercontent.com domain is blocked by Jio and
possibly other ISPs in India. This likely is due to a wise government or court
order. There is a substantial [Hacker News
thread](https://news.ycombinator.com/item?id=34231553) discussing this issue,
but the situation has been the same now, for more than a
couple of months.

The block seems to be at the DNS level and I had sucess with using
[Google's Public DNS](https://developers.google.com/speed/public-dns) server.

To change the DNS server I updated the _DNS servers_ setting in the
Jio broadband router under _Network > LAN > DNS servers_. Change the option to
select _Use Below_ and enter Google's primary and secondary DNS servers viz.
_8.8.8.8_ and _8.8.4.4._. The _DNS Servers_ setting seems to get reset to
_Use DNS Proxy_, every time I reboot the router. TODO: I need to verify this a few
more times and likely change the setting at my OS level in each device.

For some time, the DNS server change didn't seem to work. In this case, I got
unblocked by using the [Tor Browser](https://www.torproject.org/). This doesn't
help with other apps that make a request to _raw.githubusercontent.com_. I ran into
this problem again when installing [Doom Emacs](https://github.com/doomemacs/doomemacs)
which unfortunately needed to download some files from the cursed github domain.
After some Googling, I ended up using [ProxyChains](https://github.com/haad/proxychains)
to make the Doom Emacs install command to use the local tor connection.

```bash
sudo service tor start
sudo apt install proxychains
proxychains ~/.config/emacs/bin/doom install
```

Yay! I don't need to buy a VPN now, just because I cheaped out choosing Jio.

**Update:** As of 5 September, 2023, I am still unable to access content from raw.githubusercontent.com
when using Jio Broadband unless I use one of the above techniques.
