Install
=======
Install this package using [guru](https://github.com/richRemer/guru) tool.

```sh
git clone git@github.com:richRemer/btctickd.git
guru install ./btctickd
```

Setup
=====
Enable the timer service to begin tracking the price:

```sh
systemctl enable --now btctickd.timer
```

Optionally, enable the file rotation service so price data files get rotated
periodically:

```sh
systemctl enable --now btctick-rotate.timer
```

Displaying Ticker Data
======================
The ticker data will be saved to */var/local/btctick/ticker.data* and related
files.  To print all data, you can run something like:

```sh
cat /var/local/btctick/ticker.data-* /var/local/btctick/ticker.data
```
