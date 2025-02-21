# Maintainer: https://github.com/reignofshadovv
pkgname=archupdates
pkgver=1.2
pkgrel=1
pkgdesc="Arch Linux update script with user-level systemd service, timer, and a Check Updates desktop entry"
arch=('any')
url="https://example.com/archupdates"
license=('GPL')
depends=('dunst' 'libnotify' 'pacman-contrib' 'flatpak' 'yay')
source=("archupdates"
        "archupdates.service"
        "archupdates.timer"
        "archupdates.desktop")
md5sums=('SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
  # Install the update script to /usr/bin
  install -Dm755 "$srcdir/archupdates" "$pkgdir/usr/bin/archupdates"

  # Install the user systemd service file
  install -Dm644 "$srcdir/archupdates.service" "$pkgdir/usr/lib/systemd/user/archupdates.service"

  # Install the user systemd timer file
  install -Dm644 "$srcdir/archupdates.timer" "$pkgdir/usr/lib/systemd/user/archupdates.timer"

  # Install the desktop entry for "Check Updates"
  install -Dm644 "$srcdir/archupdates.desktop" "$pkgdir/usr/share/applications/archupdates.desktop"
}
