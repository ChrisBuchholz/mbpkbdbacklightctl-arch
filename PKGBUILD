# Maintainer: Chris Buchholz <christoffer.buchholz@gmail.com>
#
# mbpkbdbacklightctl - control keyboard backlight for MacBook Pro
# Copyright (C) 2010  Chris Buchholz <christoffer.buchholz@gmail.com>
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
source=(http://gitorious.org/mactel/mbpkbdbacklightctl/blobs/raw/master/src/mbpkbdbacklightctl.cpp
        mbpkbdbacklightctl.rc)
md5sums=('dfb3aa26a257590b2e784c8fb0734a72'
         '55e7d1c4d09557fad70acd8656cebd79')

build() {
    cd $srcdir/
    $CC $CFLAGS mbpkbdbacklightctl.cpp -o mbpkbdbacklightctl
}

package() {
    install -Dm755 $srcdir/mbpkbdbacklightctl $pkgdir/usr/bin/mbpkbdbacklightctl
    install -Dm755 $srcdir/mbpkbdbacklightctl.rc $pkgdir/etc/rc.d/mbpkbdbacklightctl
}
