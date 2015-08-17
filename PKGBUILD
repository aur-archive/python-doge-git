# Maintainer: uberushaximus <uberushaximus AT gmail DOT com>

pkgname=python-doge-git
_pkgname=doge
pkgver=1.0.0
pkgrel=2
pkgdesc="A simple motd script based on the slightly stupid but very funny doge meme. It prints random grammatically incorrect statements that are sometimes based on things from your computer."
arch=('any')
url="https://github.com/thiderman/doge"
license=('MIT')
depends=('python')
makedepends=('git' 'python-distribute')
source=("$pkgname"::'git://github.com/thiderman/doge.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname-build"
  git describe --long | sed -E 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "$srcdir/$pkgname"
  python setup.py install --root="$pkgdir/" --optimize=1
}

# vim:set ts=2 sw=2 et:
