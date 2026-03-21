# Maintainer: Saatvik <saatvik333sharma@gmail.com>
pkgname=sddm-theme-obscure-gruvbox-boxy-git
pkgver=r1
pkgrel=1
pkgdesc="A flat Gruvbox-dark SDDM theme based on Obscure"
arch=('any')
url="https://github.com/<your-user>/obscure-gruvbox-boxy-sddm"
license=('MIT')
depends=('sddm' 'qt6-5compat')
makedepends=('git')
provides=('sddm-theme-obscure-gruvbox-boxy')
conflicts=('sddm-theme-obscure-gruvbox-boxy')
source=("${pkgname}::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
    cd "${pkgname}"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "${pkgname}"

    install -dm755 "${pkgdir}/usr/share/sddm/themes/obscure-gruvbox-boxy"
    cp -r Main.qml theme.conf metadata.desktop README.md assets "${pkgdir}/usr/share/sddm/themes/obscure-gruvbox-boxy/"

    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
