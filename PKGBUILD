# Maintainer: Your Name <you@example.com>
pkgname=archupdates
pkgver=1.0
pkgrel=1
pkgdesc="Arch Linux updates script with user-level systemd service and timer"
arch=('any')
url="https://example.com/archupdates"
license=('GPL')
depends=()
source=("archupdates"
        "archupdates.service"
        "archupdates.timer")
md5sums=('SKIP' 'SKIP' 'SKIP')

package() {
  # Install the script to /usr/bin
  install -Dm755 "$srcdir/archupdates" "$pkgdir/usr/bin/archupdates"
  
  # Install the user service unit file to /usr/lib/systemd/user
  install -Dm644 "$srcdir/archupdates.service" "$pkgdir/usr/lib/systemd/user/archupdates.service"
  
  # Install the user timer unit file to /usr/lib/systemd/user
  install -Dm644 "$srcdir/archupdates.timer" "$pkgdir/usr/lib/systemd/user/archupdates.timer"
}
