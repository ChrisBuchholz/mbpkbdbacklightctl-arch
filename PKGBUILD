# Maintainer: Chris Buchholz <christoffer.buchholz [at] gmail [dot] com>

pkgname=mbpkbdbacklight
pkgver=0.1
pkgrel=1
pkgdesc="Automatically adjust keyboard backlight on MacBook Pro"
arch=('i686' 'x86_64')
license=('GPL3')
CC=g++
CFLAGS=(-Wall)
source=(http://gitorious.org/mactel/mbpkbdbacklight/blobs/raw/master/src/mbpkbdbacklight.cpp
        mbpkbdbacklight.rc)
md5sums=('8e24ca3e86d54b9e09a28f4fb13ac889'
         'e8e3b34be3d6418d672248078c83f6e3')

build() {
    cd $srcdir/
    $CC $CFLAGS mbpkbdbacklight.cpp -o mbpkbdbacklight
}

package() {
    install -Dm755 $srcdir/mbpkbdbacklight $pkgdir/usr/bin/mbpkbdbacklight
    install -Dm755 $srcdir/mbpkbdbacklight.rc $pkgdir/etc/rc.d/mbpkbdbacklight
}
