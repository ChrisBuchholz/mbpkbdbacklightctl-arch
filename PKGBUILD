# Maintainer: chrisbuchholz <christoffer.buchholz@gmail.com>
#
# mbpkbdbacklightctl - control keyboard backlight for MacBook Pro
# Copyright (C) 2010  chrisbuchholz <http://chrisbuchholz.me/>
#
# This file is part of mbpkbdbacklightctl
#
# mbpkbdbacklightctl is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# mbpkbdbacklightctl is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with mbpkbdbacklightctl. If not, see <http://www.gnu.org/licenses/>.

pkgname=mbpkbdbacklightctl
pkgver=0.3.1
pkgrel=1
pkgdesc="Automatically adjust keyboard backlight on MacBook Pro"
arch=('i686' 'x86_64')
depends=('libxss')
license=('GPL3')
CC=g++
CFLAGS=('-Wall -lXss')
source=(https://raw.github.com/ChrisBuchholz/mbpkbdbacklightctl/bf9e230f6f17862b3a31fffec0e5e4c7620caaa4/src/mbpkbdbacklightctl.cc
        mbpkbdbacklightctl.rc)
md5sums=('9727914082a8b6611ec6e216ae9d366a'
         'ed0cc5dc5bf48373c1d1ec142b8fd8b2')

build() {
    cd $srcdir/
    $CC $CFLAGS mbpkbdbacklightctl.cc -o mbpkbdbacklightctl
}

package() {
    install -Dm755 $srcdir/mbpkbdbacklightctl $pkgdir/usr/bin/mbpkbdbacklightctl
    install -Dm755 $srcdir/mbpkbdbacklightctl.rc $pkgdir/etc/rc.d/mbpkbdbacklightctl
}
