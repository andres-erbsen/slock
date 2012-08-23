# Maintainer: Andres Erbsen <andres.erbsen@gmail.com>
pkgname=slock
pkgver=1.1.0
pkgrel=1
pkgdesc="Suckless screen locker, patched against deadlocks"
url="https://github.com/andres-erbsen/slock"
arch=('i686' 'x86_64')
license=('MIT')
depends=(libx11)
source=(config.mk LICENSE Makefile slock.c)
md5sums=('21e7664ec78f1987857c7986ba5c0ec5'
         '56b8b04856e018b8cf643db17d0c6232'
         '9a31189e29d0be16ba63d9115bfb5f7e'
         'a4ba6a05a181ff72fb285a741a07863e')

build() {
  cd $srcdir
  make PREFIX=/usr DESTDIR=$pkgdir install || return 1
  install -m644 -D LICENSE $pkgdir/usr/share/licences/$pkgname/LICENSE
}
