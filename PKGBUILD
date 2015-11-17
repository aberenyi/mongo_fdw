# Original author: Brendan MacDonell <brendan@macdonell.net>
# Contributor:     Attila Berényi <aberenyi@gislab.hu>

pkgname='mongo_fdw'
pkgver='4.0.0'
pkgrel='1'
pkgdesc='PostgreSQL foreign data wrapper for MongoDB'
arch=('i686' 'x86_64')
url='https://github.com/EnterpriseDB/mongo_fdw'
license=('LGPL3')
depends=(postgresql)
install='mongo_fdw.install'
source=("https://github.com/EnterpriseDB/${pkgname}/archive/REL-${pkgver//\./_}.tar.gz")
md5sums=('9705f9d0c9affefa4184fb66051b7c90')

build() {
	cd "${pkgname}-REL-${pkgver//\./_}"
	./autogen.sh --with-master
	#make
}

package() {
	cd "${pkgname}-REL-${pkgver//\./_}"
	make DESTDIR="${pkgdir}/" install
}
