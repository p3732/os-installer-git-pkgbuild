# Maintainer: Peter Eisenmann <p3732 at getgoogleoff dot me>
pkgname=os-installer
pkgver=0.1.0
pkgrel=1
pkgdesc="Operating system installer, intended to be used with live systems."
arch=('any')
url="https://gitlab.gnome.org/p3732/os-installer"
license=('GPL3')
depends=('glib2' 'gnome-desktop' 'gtk3' 'libgweather' 'libhandy' 'python-gobject' 'python-yaml' 'udisks2' 'vte3')
makedepends=('git' 'ninja' 'meson')
source=("$pkgname::git+https://gitlab.gnome.org/p3732/os-installer.git?unsigned#tag=latest")
sha256sums=('SKIP')

build() {
	arch-meson $pkgname build
	meson compile -C build
}

package() {
	DESTDIR="$pkgdir" meson install -C build
}
