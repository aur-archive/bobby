# Maintainer: Daniel Nögel <arch[at]danielnoegel[dot]de>
pkgname=bobby
_upkgname=Bobby
pkgver=1.6
pkgrel=1
pkgdesc="Package for the puzzle game bobby"
url="http://www.nooskewl.com/content/Bobby/"
arch=('x86_64')
license=('custom')
depends=()
optdepends=()
makedepends=()
conflicts=()
replaces=()
backup=()
source=("http://www.nooskewl.com/stuff/downloads/${_upkgname}-${pkgver}-linux-x86_64.tar.bz2")
md5sums=('d2afcccc8c7a02b7fb9b4df8ca5adc54')

build() {
  cd "${srcdir}/${_upkgname}-${pkgver}-linux-x86_64"
}

package() {
  cd "${_upkgname}-${pkgver}-linux-x86_64"

  install -d "${pkgdir}/usr/share/bobby/data/spacestuff"
  install -d "${pkgdir}/usr/lib"
  install -d "${pkgdir}/usr/bin"

  install -Dm644 data/*.*  "${pkgdir}/usr/share/bobby/data"
  install -Dm644 data/intro  "${pkgdir}/usr/share/bobby/data"
  install -Dm644 data/spacestuff/*  "${pkgdir}/usr/share/bobby/data/spacestuff"


  install -Dm755  Bobby  "${pkgdir}/usr/share/bobby/"
  install -Dm644 libbass.so "${pkgdir}/usr/lib"
  ln -s /usr/share/bobby/Bobby "${pkgdir}/usr/bin/Bobby"  

}

