# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=nfs-utils-s6rcserv
pkgver=0.4
pkgrel=2
pkgdesc="nfs service for"
arch=(x86_64)
license=('beerware')
depends=('nfs-utils' 'rpcbind' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('nfs.prepare.dependencies'
		'nfs.prepare.type'
		'nfs.prepare.up'
		
		'rpc.mountd.longrun.dependencies'
		'rpc.mountd.longrun.finish'
		'rpc.mountd.longrun.pipeline-name'
		'rpc.mountd.longrun.producer-for'
		'rpc.mountd.longrun.run'
		'rpc.mountd.longrun.type'
		
		'rpc.mountd.log.consumer-for'
		'rpc.mountd.log.dependencies'
		'rpc.mountd.log.run'
		'rpc.mountd.log.type'
		
		'rpc.statd.longrun.dependencies'
		'rpc.statd.longrun.pipeline-name'
		'rpc.statd.longrun.producer-for'
		'rpc.statd.longrun.run'
		'rpc.statd.longrun.type'
		
		'rpc.statd.log.consumer-for'
		'rpc.statd.log.dependencies'
		'rpc.statd.log.run'
		'rpc.statd.log.type'
				
		'rpcbind.longrun.dependencies'
		'rpcbind.longrun.pipeline-name'
		'rpcbind.longrun.producer-for'
		'rpcbind.longrun.run'
		'rpcbind.longrun.type'
		
		'rpcbind.log.consumer-for'
		'rpcbind.log.dependencies'
		'rpcbind.log.run'
		'rpcbind.log.type'
		
		'bundle.nfs.contents'
		'bundle.nfs.type'
		'nfs-utils.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         '925752acc49b8310e9a819644a18cda1'
         '6acb87652f8edc7356b4f5a2b1762e3a'
         '3fac300b7b2e2f611b89ebf8227be536'
         'a4370c8d22fb6177d8e488824afee932'
         '5816ba4b4021194a3d73d6373a9fcfd0'
         'adc36877af4664f0f090c2e2d9daef9e'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '5f738836e54246478bb7033705969f94'
         '68b329da9893e34099c7d8ad5cb9c940'
         '5caf251dbb9123c031b515b52f030fe4'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'd3f4ac8e02955ca5612da316657c42d0'
         '303a65258061694c20826db6140b7124'
         '18a992b3a588666bcc311d1bfa4dca57'
         '84a5b6ea24ae6762ab5a260bb15ca81b'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '83701784cceae269279b9582333ff7fe'
         '68b329da9893e34099c7d8ad5cb9c940'
         '9051f2a93408552602a5f4fde1291614'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'd24b4fa010a8b99d8308962d68c9c963'
         'a48e013b910ed99f818a5961fd72c322'
         '6238ae821d169ef783c1a25a99e77a68'
         'b976b815ade14c80df68242f768d33ff'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '614a055336b11875f1a8355ab9b747cd'
         '68b329da9893e34099c7d8ad5cb9c940'
         '6bc73ee4eaa5b4ea1d5f6bdee2fac506'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '87cc1db5feb5c04c82696fef2b214064'
         '71abe97e2554d37f1d12c5bf4945297f'
         'efac00ab6877a1c74e94fea86b78281a'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-nfs need a maj at nfs e.g user-Dbus
	install -Dm 0644 "$srcdir/bundle.nfs.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Nfs/contents"
	install -Dm 0644 "$srcdir/bundle.nfs.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Nfs/type"
	
	# prepare
	install -Dm 0644 "$srcdir/nfs.prepare.dependencies" "$pkgdir/etc/s6-serv/available/rc/nfs-prepare/dependencies"
	install -Dm 0644 "$srcdir/nfs.prepare.type" "$pkgdir/etc/s6-serv/available/rc/nfs-prepare/type"
	install -Dm 0644 "$srcdir/nfs.prepare.up" "$pkgdir/etc/s6-serv/available/rc/nfs-prepare/up"
	
	# longrun
	install -Dm 0644 "$srcdir/rpc.mountd.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-longrun/dependencies"
	install -Dm 0644 "$srcdir/rpc.mountd.longrun.finish" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-longrun/finish"
	install -Dm 0644 "$srcdir/rpc.mountd.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/rpc.mountd.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-longrun/producer-for"
	install -Dm 0644 "$srcdir/rpc.mountd.longrun.run" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-longrun/run"
	install -Dm 0644 "$srcdir/rpc.mountd.longrun.type" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-longrun/type"
	
	## rpc.statd
	install -Dm 0644 "$srcdir/rpc.statd.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-longrun/dependencies"
	install -Dm 0644 "$srcdir/rpc.statd.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/rpc.statd.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-longrun/producer-for"
	install -Dm 0644 "$srcdir/rpc.statd.longrun.run" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-longrun/run"
	install -Dm 0644 "$srcdir/rpc.statd.longrun.type" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-longrun/type"
	
	## rpcbind
	install -Dm 0644 "$srcdir/rpcbind.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/rpcbind-longrun/dependencies"
	install -Dm 0644 "$srcdir/rpcbind.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/rpcbind-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/rpcbind.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/rpcbind-longrun/producer-for"
	install -Dm 0644 "$srcdir/rpcbind.longrun.run" "$pkgdir/etc/s6-serv/available/rc/rpcbind-longrun/run"
	install -Dm 0644 "$srcdir/rpcbind.longrun.type" "$pkgdir/etc/s6-serv/available/rc/rpcbind-longrun/type"
	
	# rpc.mountd-log
	install -Dm 0644 "$srcdir/rpc.mountd.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/consumer-for"
	install -Dm 0644 "$srcdir/rpc.mountd.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/dependencies"
	install -Dm 0644 "$srcdir/rpc.mountd.log.run" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/run"
	install -Dm 0644 "$srcdir/rpc.mountd.log.type" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/type"
	
	# rpc.statd-log
	install -Dm 0644 "$srcdir/rpc.statd.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/consumer-for"
	install -Dm 0644 "$srcdir/rpc.statd.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/dependencies"
	install -Dm 0644 "$srcdir/rpc.statd.log.run" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/run"
	install -Dm 0644 "$srcdir/rpc.statd.log.type" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/type"
	
	# rpcbind-log
	install -Dm 0644 "$srcdir/rpcbind.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/consumer-for"
	install -Dm 0644 "$srcdir/rpcbind.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/dependencies"
	install -Dm 0644 "$srcdir/rpcbind.log.run" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/run"
	install -Dm 0644 "$srcdir/rpcbind.log.type" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/nfs-utils.logd" "$pkgdir/etc/s6-serv/log.d/nfs-utils-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/nfs-utils-s6rcserv/LICENSE"
}
