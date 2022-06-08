# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Dmytri Kleiner <dk@garden.io>
pkgname=garden
pkgver=1.0.0
pkgrel=1
pkgdesc="A full-featured development framework for containers and serverless"
arch=("any")
url="https://garden.io"
options=(!strip)
license=("MPL-2.0")

package() {
  echo pwd:`pwd`
  GARDEN_DIR="$pkgdir" bash ../install.sh
  mkdir -p "${pkgdir}/opt/garden"
  mv $pkgdir/linux-amd64/* $pkgdir/opt/garden
  rmdir $pkgdir/linux-amd64
  mkdir -p "${pkgdir}/usr/bin"
  ln -s "/opt/garden/garden" "${pkgdir}/usr/bin/garden"
}
