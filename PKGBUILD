# Contributor: Nils <mail@n-sch.de>
# Maintainer: emhs <emhs08@gmail.com>
pkgname=emacs-markdown-mode-git
pkgver=2.0.r12.gb431f29
pkgrel=1
pkgdesc='Emacs markdown-mode'
arch=('i686' 'x86_64')
url='http://jblevins.org/projects/markdown-mode/'
license=('GPL')
makedepends=('git')
depends=('emacs')
install=${pkgname}.install
provides=('emacs-markdown-mode')
conflicts=('emacs-markdown-mode')
source=("$pkgname"::'git://jblevins.org/git/markdown-mode.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  # cutting off 'v' prefix that presents in the git tag
  git describe --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "$srcdir/$pkgname"
  mkdir -p $pkgdir/usr/share/emacs/site-lisp/markdown-mode
  install -Dm644 *.el $pkgdir/usr/share/emacs/site-lisp/markdown-mode
}
