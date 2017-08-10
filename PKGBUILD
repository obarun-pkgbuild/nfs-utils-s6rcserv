# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=nfs-utils-s6rcserv
pkgver=0.4
pkgrel=1
pkgdesc="nfs service for s6"
arch=(x86_64)
license=('beerware')
depends=('nfs-utils' 'rpcbind' 's6' 's6-rc' 's6-boot')
conflicts=()
install=nfs-s6rcserv.install
source=('nfs.prepare-daemon.dependencies.s6'
		'nfs.prepare-daemon.type.s6'
		'nfs.prepare-daemon.up.s6'
		
		'rpc.mountd-daemon.dependencies.s6'
		'rpc.mountd-daemon.finish.s6'
		'rpc.mountd-daemon.pipeline-name.s6'
		'rpc.mountd-daemon.producer-for.s6'
		'rpc.mountd-daemon.run.s6'
		'rpc.mountd-daemon.type.s6'
		
		'rpc.mountd-log.consumer-for.s6'
		'rpc.mountd-log.dependencies.s6'
		'rpc.mountd-log.run.s6'
		'rpc.mountd-log.type.s6'
		
		'rpc.statd-daemon.dependencies.s6'
		'rpc.statd-daemon.pipeline-name.s6'
		'rpc.statd-daemon.producer-for.s6'
		'rpc.statd-daemon.run.s6'
		'rpc.statd-daemon.type.s6'
		
		'rpc.statd-log.consumer-for.s6'
		'rpc.statd-log.dependencies.s6'
		'rpc.statd-log.run.s6'
		'rpc.statd-log.type.s6'
				
		'rpcbind-daemon.dependencies.s6'
		'rpcbind-daemon.pipeline-name.s6'
		'rpcbind-daemon.producer-for.s6'
		'rpcbind-daemon.run.s6'
		'rpcbind-daemon.type.s6'
		
		'rpcbind-log.consumer-for.s6'
		'rpcbind-log.dependencies.s6'
		'rpcbind-log.run.s6'
		'rpcbind-log.type.s6'
		
		'bundle.nfs.contents.s6'
		'bundle.nfs.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '85bceea1fb94d4166f24496dc40a35e6'
         '925752acc49b8310e9a819644a18cda1'
         '1324d4fd713ef8fc291400c585f82e70'
         '3fac300b7b2e2f611b89ebf8227be536'
         'a4370c8d22fb6177d8e488824afee932'
         '5816ba4b4021194a3d73d6373a9fcfd0'
         'adc36877af4664f0f090c2e2d9daef9e'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'a9a49ba305cc4b1bc3cfe468ca825319'
         '68b329da9893e34099c7d8ad5cb9c940'
         '5caf251dbb9123c031b515b52f030fe4'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'efa36af2fd2ad54e8555f22df8a48c55'
         '303a65258061694c20826db6140b7124'
         '18a992b3a588666bcc311d1bfa4dca57'
         '84a5b6ea24ae6762ab5a260bb15ca81b'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'ba40ddcb7769bf1f88bb7b138427fee7'
         '68b329da9893e34099c7d8ad5cb9c940'
         '9051f2a93408552602a5f4fde1291614'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'd24b4fa010a8b99d8308962d68c9c963'
         'a48e013b910ed99f818a5961fd72c322'
         '6238ae821d169ef783c1a25a99e77a68'
         'b976b815ade14c80df68242f768d33ff'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '4ed4a1547402cae76ee984b00c8a892d'
         '68b329da9893e34099c7d8ad5cb9c940'
         '6bc73ee4eaa5b4ea1d5f6bdee2fac506'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '4e8ed88bb21747d1b9622e940fd4ea0b'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-nfs need a maj at nfs e.g user-Dbus
	install -Dm 0644 "$srcdir/bundle.nfs.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Nfs/contents"
	install -Dm 0644 "$srcdir/bundle.nfs.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Nfs/type"
	
	# prepare
	install -Dm 0644 "$srcdir/nfs.prepare-daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/nfs-prepare/dependencies"
	install -Dm 0644 "$srcdir/nfs.prepare-daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/nfs-prepare/type"
	install -Dm 0644 "$srcdir/nfs.prepare-daemon.up.s6" "$pkgdir/etc/s6-serv/available/rc/nfs-prepare/up"
	
	# daemon
	install -Dm 0644 "$srcdir/rpc.mountd-daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-daemon/dependencies"
	install -Dm 0644 "$srcdir/rpc.mountd-daemon.finish.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-daemon/finish"
	install -Dm 0644 "$srcdir/rpc.mountd-daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/rpc.mountd-daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-daemon/producer-for"
	install -Dm 0644 "$srcdir/rpc.mountd-daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-daemon/run"
	install -Dm 0644 "$srcdir/rpc.mountd-daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-daemon/type"
	
	## rpc.statd
	install -Dm 0644 "$srcdir/rpc.statd-daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-daemon/dependencies"
	install -Dm 0644 "$srcdir/rpc.statd-daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/rpc.statd-daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-daemon/producer-for"
	install -Dm 0644 "$srcdir/rpc.statd-daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-daemon/run"
	install -Dm 0644 "$srcdir/rpc.statd-daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-daemon/type"
	
	## rpcbind
	install -Dm 0644 "$srcdir/rpcbind-daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-daemon/dependencies"
	install -Dm 0644 "$srcdir/rpcbind-daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/rpcbind-daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-daemon/producer-for"
	install -Dm 0644 "$srcdir/rpcbind-daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-daemon/run"
	install -Dm 0644 "$srcdir/rpcbind-daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-daemon/type"
	
	# rpc.mountd-log
	install -Dm 0644 "$srcdir/rpc.mountd-log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/consumer-for"
	install -Dm 0644 "$srcdir/rpc.mountd-log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/dependencies"
	install -Dm 0644 "$srcdir/rpc.mountd-log.run.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/run"
	install -Dm 0644 "$srcdir/rpc.mountd-log.type.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.mountd-log/type"
	
	# rpc.statd-log
	install -Dm 0644 "$srcdir/rpc.statd-log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/consumer-for"
	install -Dm 0644 "$srcdir/rpc.statd-log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/dependencies"
	install -Dm 0644 "$srcdir/rpc.statd-log.run.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/run"
	install -Dm 0644 "$srcdir/rpc.statd-log.type.s6" "$pkgdir/etc/s6-serv/available/rc/rpc.statd-log/type"
	
	# rpcbind-log
	install -Dm 0644 "$srcdir/rpcbind-log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/consumer-for"
	install -Dm 0644 "$srcdir/rpcbind-log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/dependencies"
	install -Dm 0644 "$srcdir/rpcbind-log.run.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/run"
	install -Dm 0644 "$srcdir/rpcbind-log.type.s6" "$pkgdir/etc/s6-serv/available/rc/rpcbind-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/nfs-utils-s6rcserv/LICENSE"
}
