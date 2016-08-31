# $Id: PKGBUILD 165985 2016-03-10 18:31:18Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Dag Odenhall <dag.odenhall@gmail.com>
# Contributor: Grigorios Bouzakis <grbzks@gmail.com>

pkgname=dwm
pkgver=6.1
pkgrel=3
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft' 'freetype2' 'st' 'dmenu')
install=dwm.install
source=(http://dl.suckless.org/dwm/dwm-$pkgver.tar.gz
	config.h
	dwm.desktop)
md5sums=('f0b6b1093b7207f89c2a90b848c008ec'
         '80c4ef2a3eca0fe2d14e2203e3833200'
         '939f403a71b6e85261d09fc3412269ee')

prepare() {
  cd $srcdir/$pkgname-$pkgver
  cp $srcdir/config.h config.h
}

build() {
  cd $srcdir/$pkgname-$pkgver
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11 FREETYPEINC=/usr/include/freetype2
}

package() {
  cd $srcdir/$pkgname-$pkgver
  make PREFIX=/usr DESTDIR=$pkgdir install
  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
  install -m644 -D README $pkgdir/usr/share/doc/$pkgname/README
  install -m644 -D $srcdir/dwm.desktop $pkgdir/usr/share/xsessions/dwm.desktop
}
md5sums=('f0b6b1093b7207f89c2a90b848c008ec'
         'daea98f00374033c164a05203f8066f7'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('f0b6b1093b7207f89c2a90b848c008ec'
         '80c4ef2a3eca0fe2d14e2203e3833200'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('f0b6b1093b7207f89c2a90b848c008ec'
         '03c275c0eb2fb6daaa6a24dd89350b53'
         '939f403a71b6e85261d09fc3412269ee')
md5sums=('f0b6b1093b7207f89c2a90b848c008ec'
         'be21f25f0f25f6f972aa9574e8a28322'
         '939f403a71b6e85261d09fc3412269ee')
