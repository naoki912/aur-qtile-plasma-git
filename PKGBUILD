# Maintainer: Naoki Kanazawa <nk dot naoki912 at gmail dot com>
pkgname=qtile-plasma-git
pkgver=v1.5.5.r1.g4b57f31
pkgrel=3
pkgdesc="A flexible, tree-based layout for Qtile"
arch=('any')
license=('MIT')
url='https://github.com/numirias/qtile-plasma'
depends=('qtile')
makedepends=('python-setuptools' 'git')
install=$pkgname.install
source=("${pkgname}::git://github.com/numirias/qtile-plasma.git")
sha256sums=('SKIP')

pkgver() {
  cd "$pkgname"
  git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
  cd "${srcdir}/${pkgname}"
  python setup.py install --root="${pkgdir}"
}
