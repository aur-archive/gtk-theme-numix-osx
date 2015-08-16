pkgname=gtk-theme-numix-osx
pkgver=2.ea4c2bd
pkgrel=1
pkgdesc=A modified version of the Numix GTK theme modeled to look somewhat like OSX
arch=('any')
license=('GPL3')
url='https://github.com/samhorlbeck/Numix-OSX/'
depends=('gtk-engine-murrine')
source=("git+git://github.com/samhorlbeck/Numix-OSX.git")
makedepends=('git')
md5sums=('SKIP')

pkgver() {
  cd ${srcdir}/Numix-OSX
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

build() {
	cd Numix-OSX
	rm -rf .git .gitignore
}

package() {
	cd Numix-OSX
	for FILE in $(find -type f);do
		install -D -m0644 ${FILE} ${pkgdir}/usr/share/themes/Numix-OSX/${FILE}
	done
}