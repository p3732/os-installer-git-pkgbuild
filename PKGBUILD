# Maintainer: Peter Eisenmann <p3732 at getgoogleoff dot me>
pkgname=os-installer
pkgver=0.1.2
pkgrel=1
pkgdesc="Operating system installer, intended to be used with live systems."
arch=('any')
url="https://gitlab.gnome.org/p3732/os-installer"
license=('GPL3')
depends=('glib2' 'gnome-desktop' 'gtk4' 'libadwaita' 'libgweather-4' 'python-gobject' 'python-yaml' 'udisks2' 'vte4')
makedepends=('blueprint-compiler' 'git' 'ninja' 'meson')
source=("$pkgname::git+$url.git?unsigned#tag=$pkgver")
sha256sums=('SKIP')

build() {
	arch-meson $pkgname build
	meson compile -C build
}

package() {
	DESTDIR="$pkgdir" meson install -C build
}

