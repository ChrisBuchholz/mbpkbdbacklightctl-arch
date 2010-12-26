# Maintainer: Chris Buchholz <christoffer.buchholz [at] gmail [dot] com>

pkgname=mbpkbdbacklightctl
pkgver=0.3.1
pkgrel=1
pkgdesc="Automatically adjust keyboard backlight on MacBook Pro"
arch=('i686' 'x86_64')
depends=('libxss')
license=('GPL3')
CC=g++
CFLAGS=('-Wall -lXss')
source=(http://gitorious.org/mactel/mbpkbdbacklight/blobs/raw/master/src/mbpkbdbacklightctl.cpp
        mbpkbdbacklightctl.rc)
md5sums=('64abc81c09183a357cb4a478962c4f33'
         'd202e5d2f548d8f005d1c37f026b64dc')

build() {
    cd $srcdir/
    $CC $CFLAGS mbpkbdbacklightctl.cpp -o mbpkbdbacklightctl
}

package() {
    install -Dm755 $srcdir/mbpkbdbacklightctl $pkgdir/usr/bin/mbpkbdbacklightctl
    install -Dm755 $srcdir/mbpkbdbacklightctl.rc $pkgdir/etc/rc.d/mbpkbdbacklightctl
}
