+++
title = "Access raw.githubusercontent.com files in India"
date = 2023-01-18
updated = 2023-03-20
+++


As of January 2023, raw.githubusercontent.com domain is blocked by Jio and
possibly other ISPs in India. This likely is due to a wise government or court
order. There is a substantial [Hacker News
thread](https://news.ycombinator.com/item?id=34231553) discussing this issue,
but the situation has been the same now, for more than a
couple of months.

Until it is fixed, the best way to get unblocked is likely using the [Tor
Browser](https://www.torproject.org/).

Well, today in March, I ran into this problem again when installing [Doom
Emacs](https://github.com/doomemacs/doomemacs)
which unfortunately needed to download some files from the cursed github domain.
After some Googling, I ended up using [ProxyChains](https://github.com/haad/proxychains)
to make the Doom Emacs install command to use the local tor connection.

```bash
sudo service tor start
sudo apt install proxychains
proxychains ~/.config/emacs/bin/doom install
```

Yay! I don't need to buy a VPN now, just because I cheaped out choosing Jio.

**Update:** As of 20 March, 2023, I am able to access content from raw.githubusercontent.com
