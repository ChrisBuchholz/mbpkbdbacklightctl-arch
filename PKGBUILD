# Maintainer: Chris Buchholz <christoffer.buchholz [at] gmail [dot] com>

pkgname=mbpkbdbacklight
pkgver=0.1
pkgrel=1
pkgdesc="Automatically adjust keyboard backlight on MacBook Pro"
arch=('i686' 'x86_64')
license=('GPL3')
CC=g++
CFLAGS=(-c -Wall)
source=(https://github.com/ChrisBuchholz/mbpkbdbacklight/tarball/master 
        mbpkbdbacklight.rc)
md5sums=('2e18a9ecbed93ead934e1e2af22b7d56'
         'e8e3b34be3d6418d672248078c83f6e3')

build() {
    cd $srcdir/
    $CC $CFLAGS ChrisBuchholz-mbpkbdbacklight-*/src/mbpkbdbacklight.cpp -o mbpkbdbacklight
}

package() {
    install -Dm755 $srcdir/mbpkbdbacklight $pkgdir/usr/bin/mbpkbdbacklight
    install -Dm755 $srcdir/mbpkbdbacklight.rc $pkgdir/etc/rc.d/mbpkbdbacklight
}
