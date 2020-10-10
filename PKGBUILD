# Maintainer: Stefans Mezulis <stefans.mezulis@gmail.com>
pkgname=systemd-post-suspend
pkgver=0.0.1
pkgrel=1
epoch=0
pkgdesc="Post-suspend hooks."
arch=('any')
url="https://github.com/StefansM/$pkgname"
license=('GPL')
groups=()
depends=('xorg-xkbcomp' 'xorg-xset')
makedepends=()
optdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname::git+https://github.com/StefansM/$pkgname.git")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
    cd "$pkgname"
    local version=$(git describe --tags)
    # Strip leading "v", replace first "-" with "r" and all subsequent "-"
    # with "." to make a legal Arch version number.
    version=${version#v}
    version=${version/-/r}
    version=${version//-/.}
    echo "$version"
}

package() {
    cd "$pkgname"
    install -D -m644 -t "$pkgdir/usr/lib/systemd/user" "resume@.service"
}
