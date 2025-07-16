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
