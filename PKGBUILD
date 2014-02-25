# Maintainer: Andrew Warren-Love <andrew@awarrenlove.com>
pkgname=pacmirror-git
_pkgname=pacmirror
pkgver=2.b11536f
pkgrel=1
epoch=
pkgdesc="Update the pacman mirror list using reflector"
arch=('any')
url="https://github.com/awarrenlove/pacmirror"
license=('MIT')
depends=('python3')
provides=('pacmirror')
source=('git://github.com/awarrenlove/pacmirror.git')
md5sums=('SKIP')

pkgver() {
	cd "$srcdir/$_pkgname"
	echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
	cd "$srcdir/$_pkgname"

	install -D -m755 pacmirror ${pkgdir}/usr/bin/pacmirror
	install -D -m644 pacmirror.conf ${pkgdir}/etc/pacmirror/pacmirror.conf
	install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/pacmirror/LICENSE
}

