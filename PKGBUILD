# Maintainer: Alexander Baldeck <alex.bldck@gmail.com> 
pkgname=nvidia-fancontrol
pkgver=0.5.1
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
backup=('etc/default/nvidia-fancontrol')
md5sums=('2884a4b11b0ec65b1a018772ccfed9f9'
         '035f47fb5639bb254dd570e9533653f1'
         'd6498a0369c36d80689aa0e2f9547b58'
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
