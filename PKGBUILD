# Maintainer:

_author=
_pkgname=
pkgname=${_pkgname}-git
pkgver=1
pkgrel=1
pkgdesc=''
arch=(
# 'any'
  'x86_64'
)

url='https://github.com/'
license=('GPL3')
dependencies=()
makedepends=('git')
source=("git://github.com/$_author/$_pkgname")
sha256sums=('SKIP')

prepare() {
  cd "$srcdir/$_pkgname"
  git submodule init
  git submodule update
  git fetch --tags
}

pkgver () {
  cd "$srcdir/$_pkgname"
  git describe --tags --long | sed -r 's/^v//;s/-RC/RC/;s/([^-]*-g)/r\1/;s/-/./g'
}

build() {
  cd "$srcdir/$_pkgname"
  make
}

check() {
  cd "$srcdir/$_pkgname"
# make test
}

package() {
  cd "$srcdir/$_pkgname"
  INSTALL_ROOT="$pkgdir" make install
}
