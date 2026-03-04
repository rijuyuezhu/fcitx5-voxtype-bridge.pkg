# Maintainer: Felix Yan <felixonmars@archlinux.org>
# Contributor: csslayer <wengxt AT gmail com>

pkgname=fcitx5-voxtype-bridge
pkgver=0.2.0
pkgrel=1
pkgdesc="Bridge to Voxtype voice-to-text service"
arch=('x86_64')
url="https://github.com/rijuyuezhu/fcitx5-voxtype-bridge"
license=('GPL')
depends=('fcitx5')
makedepends=('git' 'extra-cmake-modules' 'ninja')

source=("git+https://github.com/rijuyuezhu/fcitx5-voxtype-bridge.git#tag=v$pkgver")
sha512sums=('SKIP')

build() {
  cd $pkgname
  cmake -GNinja -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_INSTALL_LIBDIR=/usr/lib .
  ninja
}

package() {
  cd $pkgname
  DESTDIR="$pkgdir" ninja install
}
