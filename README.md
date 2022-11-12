## Void Linux template file for xbps-src

Instructions for building `picom-jonaburg` on void linux using `xbps-src`:

1. Setup the `void-packages` repo:

```sh
❯ git clone --depth=1 https://github.com/void-linux/void-packages
❯ cd void-packages
❯ ./xbps-src binary-bootstrap
❯ echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf
```

2. Download the template repo and copy into `srcpkgs`:

```sh
❯ git clone https://github.com/oxSleep/picom-jonaburg-template
❯ mv picom-jonaburg-template ./srcpkgs/picom-jonaburg
```

3. Build & install the package:

```sh
❯ ./xbps-src pkg picom-jonaburg
❯ sudo xbps-install --repository=hostdir/binpkgs picom-jonaburg 
```
