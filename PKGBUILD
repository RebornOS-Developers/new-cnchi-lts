# Maintainer: Rafael <rafael@rebornos.org>

pkgname=new-cnchi-lts
_pkgname2=new-cnchi-code-lts
_pkgname3=locale
pkgver=20210625
pkgrel=2
pkgdesc='New cnchi LTS code installer'
arch=('any')
url='https://gitlab.com/rebornos-team/installers/cnchi/code'
license=('GPL3')
source=("git+${url}/${_pkgname2}"
        "git+${url}/${_pkgname3}")
sha256sums=('SKIP'
            'SKIP')

pkgver() {
    date +%Y%m%d
}


package() {
    install -d ${pkgdir}/usr/share/cnchi
    install -d ${pkgdir}/usr/share/locale
    cp -r ${srcdir}/${_pkgname2}/* ${pkgdir}/usr/share/cnchi
    cp -r ${srcdir}/${_pkgname3}/${_pkgname3}/* ${pkgdir}/usr/share/${_pkgname3}
    find ${pkgdir}/usr/share/cnchi -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/locale -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/cnchi -type d -exec chmod 755 {} \;
    find ${pkgdir}/usr/share/locale -type d -exec chmod 755 {} \;
    }

