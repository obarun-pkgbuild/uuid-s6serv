# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=uuidd-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="uuidd service for s6"
arch=(x86_64)
license=('beerware')
depends=('util-linux' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('uuidd.daemon.run.s6'
		'uuidd.log.run.s6'
		'uuidd.logd'
		'LICENSE')
md5sums=('33a93824e8b9793b39025ef626e65da2'
         'ecdc4dcef90675d76115fab5b93fe2d5'
         'bed6caf6d01125b6446c1be37f7238e9'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/uuidd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/uuidd/run"
	
	# log
	install -Dm 0755 "$srcdir/uuidd.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/uuidd/log/run"
	install -Dm 0644 "$srcdir/uuidd.logd" "$pkgdir/etc/s6-serv/log.d/serv/uuidd"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/uuidd-s6serv/LICENSE"
}
