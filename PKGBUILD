# Maintainer: echo -n 'bWF0dEBnZXRjcnlzdC5hbA==' | base64 --decode

pkgname=citrine
pkgver=3.4.7
pkgrel=1
pkgdesc="Crystal Linux Script for installing the system"
arch=('any')
url="https://git.tar.black/crystal/programs/citrine"
license=('custom')
source=("citrine.sh" "citrine.internal.sh")
depends=('arch-install-scripts' 'util-linux' 'parted' 'dialog' 'dosfstools' 'ntp' 'python' 'wget')
md5sums=('c16f9c01d656886b905071cb5477d3e3'
         '7791c00338bc02682538b696343f2e39')

package() {
    chmod +x *.sh
    mkdir -p ${pkgdir}/usr/bin
    mkdir -p ${pkgdir}/etc/citrine
    echo $pkgver > ${pkgdir}/etc/citrine/version
    cp citrine.sh ${pkgdir}/usr/bin/citrine
    cp citrine.internal.sh ${pkgdir}/usr/bin/citrine.internal
}
