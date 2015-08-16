# Maintainer: Tino Reichardt <milky-archlinux@mcmilk.de>
pkgname=mmix
pkgver=0.3
pkgrel=1
pkgdesc="small console mixer"
arch=('x86_64' 'i686')
license=('GPLv2')
source=(http://www.mcmilk.de/projects/mmix/dl/$pkgname-$pkgver.tar.bz2)
url="http://www.mcmilk.de/projects/mmix/"
md5sums=('81f16ef839c1fab2c0a867cbbbaa9c73')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  install -d -Dm755 ${pkgdir}/usr/bin
  install -d -Dm755 ${pkgdir}/usr/share/man/man1

  install -m755 mmix ${pkgdir}/usr/bin
  install -m644 doc/mmix.1 ${pkgdir}/usr/share/man/man1
}
