# Maintainer: Peter Eisenmann <p3732 at getgoogleoff dot me>
pkgname=os-installer
pkgver=0.1.2
pkgrel=1
pkgdesc="Operating system installer, intended to be used with live systems."
arch=('any')
url="https://gitlab.gnome.org/p3732/os-installer"
license=('GPL3')
depends=('epiphany' 'glib2' 'gnome-control-center' 'gnome-desktop' 'gnome-disk-utility' 'gtk3' 'libgweather' 'libhandy' 'python-gobject' 'python-yaml' 'udisks2' 'vte3')
makedepends=('git' 'ninja' 'meson')
source=("$pkgname::git+$url.git?unsigned#tag=$pkgver")
sha256sums=('SKIP')

build() {
	arch-meson $pkgname build
	meson compile -C build
}

package() {
	DESTDIR="$pkgdir" meson install -C build
}

