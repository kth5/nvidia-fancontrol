# Maintainer: Alexander Baldeck <alex.bldck@gmail.com> 
pkgname=nvidia-fancontrol
pkgver=0.5
pkgrel=1
pkgdesc="Simple Nvidia Fan control script"
arch=(x86_64)
url="https://github.com/kth5/hackinez.git"
license=('GPL3')
depends=('xorg-server' 'xorg-xinit' 'nvidia-settings' 'nvidia-dkms')
source=('nvidia-fancontrol'
        'nvidia-fancontrol-x'
        'nvidia-fancontrol.default'
        'dfp-edid.bin'
        'xorg.conf')
md5sums=('99a2d078145a59e69a34937a7647d047'
         '97582cf6a7789bd53587b1dd23a757d7'
         '0367aea08017d96ac1a30721ac7c3bdf'
         '737a37ad8382bbfde91b5e9e81089a7d'
         'f51916f26f7d50dd4f84b57f0b83e176')

package() {
	cd ${srcdir}
	install -D -m755 ${srcdir}/nvidia-fancontrol ${pkgdir}/opt/nvidia-fancontrol/nvidia-fancontrol
	install -D -m755 ${srcdir}/nvidia-fancontrol-x ${pkgdir}/opt/nvidia-fancontrol/nvidia-fancontrol-x
	install -D -m644 ${srcdir}/nvidia-fancontrol.default ${pkgdir}/etc/default/nvidia-fancontrol
	install -m644 ${srcdir}/dfp-edid.bin ${pkgdir}/opt/nvidia-fancontrol/dfp-edid.bin
	install -m644 ${srcdir}/xorg.conf ${pkgdir}/opt/nvidia-fancontrol/xorg.conf
}
