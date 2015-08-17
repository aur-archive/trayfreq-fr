# Contributor: Devin Smittle <pandagoat@gmail.com>
# Contributor: Arnaud Durand-Favreau <biginoz@free.fr>
pkgname=trayfreq-fr
_pkgname=trayfreq
pkgver=0.2.x.dev2
_pkgver=0.2.x-dev2
pkgrel=180
pkgdesc="trayfreq-fr is in program in french translation of trayfreq .It 
let's you control your CPU frequency . 
http://wiki.archlinux.fr/howto/cpufreq#trayfreq"
arch=('i686' 'x86_64')
url="http://trayfreq.sourceforge.net"
license=('GPL')
groups=()
depends=('gtk2' 'cpupower' 'libacpi')
makedepends=('pkgconfig' 'gtk2')
provides=()
conflicts=()
replaces=(trayfreq)
backup=()
install=$_pkgname.install
source=(http://downloads.sourceforge.net/$_pkgname/$_pkgname-$_pkgver.tar.gz 
trayfreq-0.2.x-dev2-fr-179.diff)
md5sums=('1a97ce007090ddee591f213e71968f78' 
'aa7fc129cc81941af8b361318fe2467e')
noextract=()

build() {
  patch -p0 < ../trayfreq-0.2.x-dev2-fr-179.diff
  cd "$srcdir/$_pkgname-$_pkgver"

  ./configure --prefix=/usr --disable-setsuid
  make || return 1
  make DESTDIR="$pkgdir/" install
}
