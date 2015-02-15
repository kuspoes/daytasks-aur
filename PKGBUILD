# Maintainer: Kusaeni <kusaeni[at]gmail.com>
pkgname=daytasks
pkgver=2.8.2
pkgrel=2
pkgdesc="DayTasks is a minimal todo.txt-compatible app"
url="https://burnsoftware.wordpress.com/daytasks/"
arch=('x86_64' 'i686')
license=('GPLv3')
depends=('vala')
makedepends=('gcc')
#install='daytask.install'
source=("https://launchpad.net/~thejambi/+archive/ubuntu/thejambi/+files/daytasks_2.8.2.orig.tar.gz")
md5sums=('da1269dccc184fd8ffe845e2286bfccc')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}

# vim:set ts=2 sw=2 et:
