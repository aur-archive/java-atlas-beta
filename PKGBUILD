# Maintainer: Corey Mwamba <contact.me@coreymwamba.co.uk>
# Contributor: Corey Mwamba <contact.me@coreymwamba.co.uk>
pkgname=java-atlas-beta
pkgver=1.2.13
pkgrel=1
pkgdesc="A Java map and navigation application using offline vector maps"
arch=('any')
url="http://wiki.openstreetmap.org/wiki/Atlas_(navigation_application)"
license=('unknown')
depends=('java-runtime')
_pkgname=Atlas-Beta
source=(http://www.talent.gr/public/atlas/$_pkgname-$pkgver.zip)
md5sums=('0c90f1321b421bee58314a0be155aeae')
noextract=($_pkgname-$pkgver.zip)
makedepends=('zip')
install=('java-atlas-beta.install')

package(){
mkdir -p $pkgdir/opt
unzip $_pkgname-$pkgver.zip -d $pkgdir/opt
mkdir -p $pkgdir/usr/bin
echo "#!/usr/bin/bash
exec /usr/bin/java -jar /opt/$_pkgname-$pkgver/$_pkgname.jar $@" > $pkgdir/usr/bin/atlas-beta
chmod +x $pkgdir/usr/bin/atlas-beta
}
