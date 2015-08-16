
pkgname=kscope4
pkgver=1.7.0
pkgrel=2
pkgdesc="Is the port to KDE4 / Qt4 of Kscope-1.6.0 by Elad Lahav, a GUI frontend for cscope."
arch=('i686' 'x86_64')
url="https://opendesktop.org/content/show.php/Kscope4?content=156987"
depends=('kdebase-runtime' 'kdebase-katepart')
makedepends=('cmake' 'automoc4' 'gcc')
source=("https://opendesktop.org/CONTENT/content-files/156987-$pkgname-$pkgver.tar.xz")
license=('GPL')
install=${pkgname}.install
md5sums=('7231310955c5460c1c705667d55bf208')

build() {
  
  cd ${srcdir}/${pkgname}-$pkgver
  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` \
    -DCMAKE_BUILD_TYPE=Release
  make
}

package() {
  cd ${srcdir}/${pkgname}-$pkgver
  make DESTDIR=$pkgdir install
}
