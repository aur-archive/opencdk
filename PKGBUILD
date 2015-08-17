# $Id: PKGBUILD 144390 2011-12-05 13:20:55Z jgc $
# Maintainer: Jan de Groot <jgc@archlinux.org>

pkgname=opencdk
pkgver=0.6.6
pkgrel=3
pkgdesc="The Open Crypto Development Kit provides basic parts of the OpenPGP message format"
arch=('i686' 'x86_64')
url="http://www.gnu.org/software/gnutls/"
license=('GPL')
depends=('libgcrypt' 'zlib')
options=('!libtool')
source=(ftp://ftp.gnutls.org/pub/gnutls/attic/opencdk/opencdk-${pkgver}.tar.bz2)
md5sums=('813d62d7afe7b2c2d8f3df0a6c9d9331')

build() {
  cd ${srcdir}/${pkgname}-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install
}
