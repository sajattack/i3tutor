# Maintainer Paul Sajna <sajattack@gmail.com>

pkgname='i3tutor-git'
pkgver=1.0
pkgrel=1
pkgdesc='Vimtutor for i3wm'
arch=('any')
url='https://github.com/sajattack/i3tutor'
license=('MIT')
depends=('i3-wm' 'xorg-server-xephyr')
makedepends=('git' 'sed')
source=("git+https://github.com/sajattack/i3tutor")
sha1sums=('SKIP')

prepare() {
  cd "$srcdir/i3tutor/"
}

package() {
  cd "$srcdir/i3tutor/"

  mkdir -p "$pkgdir/usr/bin"
  mkdir -p "$pkgdir/usr/share/i3tutor"
  cp -a --no-preserve=ownership * "$pkgdir/usr/share/i3tutor"
  ln -s "$pkgdir/usr/share/i3tutor/i3tutor" "$pkgdir/usr/bin/"
  chmod +x "$pkgdir/usr/bin/i3tutor"
}
