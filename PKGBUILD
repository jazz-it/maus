# Maintainer: Georg Wagner <puxplaying_at_gmail_dot_com>

pkgname=maus
pkgver=1.1
pkgrel=1
pkgdesc="Bash script to update and maintain a Manjaro or Arch system"
arch=(any)
url="https://github.com/puxplaying/manjaro-update"
license=('GPL3')
depends=('pacman' 'pacman-contrib' 'sudo' 'bash')
makedepends=('git')
optdepends=('meld: Needed for diff operations'
	'reflector: Needed for Arch mirrorlist update')
conflicts=(manjaro-update)
source=("$pkgname-$pkgver.tar.gz::$url/archive/$pkgver.tar.gz")
sha256sums=('34ee877256950ae64438113a4248364cf2bf35f599ea062aa1b9dbda4fd932c7')

package() {
	cd "$srcdir/$pkgname-$pkgver"
	install -Dm644 "update.desktop" "$pkgdir/usr/share/applications/update.desktop"
	install -Dm644 "update.png" "$pkgdir/usr/share/pixmaps/update.png"
	install -Dm755 "$srcdir/$pkgname-$pkgver/$pkgname" "$pkgdir/usr/bin/$pkgname"
}
