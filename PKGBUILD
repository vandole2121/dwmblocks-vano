pkgname=dwmblocks
pkgver=1.0
pkgrel=1
pkgdesc="dwmblocks customised"
url="https://github.com/torrinfail/dwmblocks"
arch=('i686' 'x86_64')
license=('MIT')
options=()
depends=()
source=(git+https://github.com/torrinfail/dwmblocks.git#tag=master
        blocks.h)
sha256sums=('SKIP'
            'SKIP')

prepare() {
  cd "$srcdir/$pkgname"
  cp "$srcdir/blocks.h" blocks.h
}

build() {
  cd "$srcdir/$pkgname"
  make 
}

package() {
  cd "$srcdir/$pkgname"
  make PREFIX=/usr DESTDIR="$pkgdir" install
}
