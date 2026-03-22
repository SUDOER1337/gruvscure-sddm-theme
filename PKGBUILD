# Maintainer: SUDOER1337
pkgname=sddm-theme-gruvscure-git
pkgver=r28.784c2a3
pkgrel=1
pkgdesc="A flat Gruvbox-dark SDDM theme based on Obscure"
arch=('any')
url="https://github.com/SUDOER1337/gruvscure-sddm-theme"
license=('MIT')
depends=('sddm' 'qt6-5compat')
makedepends=('git')
provides=('sddm-theme-gruvscure')
conflicts=('sddm-theme-gruvscure')
source=("${pkgname}::git+${url}.git")
sha256sums=('SKIP')

pkgver() {
    cd "${pkgname}"
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "${pkgname}"

    install -dm755 "${pkgdir}/usr/share/sddm/themes/gruvscure-sddm-theme"
    cp -r Main.qml theme.conf metadata.desktop README.md assets "${pkgdir}/usr/share/sddm/themes/gruvscure-sddm-theme/"

    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
