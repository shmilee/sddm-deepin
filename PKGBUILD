# Maintainer: shmilee

_theme='deepin'

pkgname=sddm-theme-deepin
pkgver=r22.5cd941c
pkgrel=1
pkgdesc="Deepin style SDDM theme by Match-Yang"
arch=('any')
url="https://github.com/Match-Yang/sddm-deepin"
license=('CCPL:cc-by-sa')
depends=('sddm' 'qt5-graphicaleffects')
conflicts=('sddm-theme-deepin-git')
source=("git+https://github.com/shmilee/${pkgname}.git")
md5sums=('SKIP')

pkgver() {
    cd ${pkgname}
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd ${pkgname}/${_theme}
    find . -type f -exec install -Dm644 {} "${pkgdir}"/usr/share/sddm/themes/${_theme}/{} \;
    find . -type l -exec cp -P {} "${pkgdir}"/usr/share/sddm/themes/${_theme}/{} \;
}
