# Maintainer: Jakub Kozisek <nodevel at gmail dot com>

pkgname=libtvdb
pkgver=0.3.0
pkgrel=3
pkgdesc="A small library to fetch TV series information from the thetvdb.com web service"
arch=('any')
url="http://libtvdb.sourceforge.net/"
license=('GPLv2')
depends=('kdebase-runtime>=4.5.80')
makedepends=('cmake')
source=(http://downloads.sourceforge.net/project/$pkgname/0.3/$pkgname-$pkgver.tar.bz2)

build() {
  cd ${srcdir}/$pkgname-$pkgver
  cmake -DCMAKE_INSTALL_PREFIX=$( kde4-config --prefix ) -DCMAKE_BUILD_TYPE=Release ./
  make || return 1
  make DESTDIR=$pkgdir install || return 1
}
md5sums=('7ce5ca5ffc9a50ee8c8c695dd973dfcf')