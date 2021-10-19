# Maintainer: Rafael <rafael@rebornos.org>
# PKGBUILD modified for use with Github code

pkgname=new-cnchi-lts
codename=new-cnchi-code-lts
lname=locale
ccommit=e8a35cadfa1502b43f710caf7a0fe3c2d1f6f6a7
lcommit=c3d06a98b584e533537d022995a1bba1477b78ba
pkgver=20211019
pkgrel=1
pkgdesc='New cnchi lts code installer. Do not install it on a computer that is already running RebornOS.'
arch=('any')
url='https://github.com/RebornOS-Developers'
license=('GPL3')
depends=(git)
source=("git+${url}/${codename}#commit=${ccommit}"
        "git+${url}/${lname}#commit=${lcommit}")
sha256sums=('SKIP' 'SKIP')

pkgver() {
    date +%Y%m%d
     }

package() {
    install -d ${pkgdir}/usr/share/cnchi
    install -d ${pkgdir}/usr/share/locale
    install -d ${pkgdir}/usr/share/licenses/${pkgname}
    cp -r ${srcdir}/${codename}/* ${pkgdir}/usr/share/cnchi
    cp -r ${srcdir}/${lname}/${lname}/* ${pkgdir}/usr/share/${lname}
    install -m 644 ${srcdir}/${codename}/LICENSE ${pkgdir}/usr/share/licenses/${pkgname}
    find ${pkgdir}/usr/share/cnchi -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/locale -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/cnchi -type d -exec chmod 755 {} \;
    find ${pkgdir}/usr/share/locale -type d -exec chmod 755 {} \;
    }

