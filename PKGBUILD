# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Henrik Voß <hennevoss@gmail.com>
pkgname=openhab-designer
pkgver=1.7.1
pkgrel=1
pkgdesc="openHAB automation designer"
arch=('x86_64')
url="http://www.openhab.org/"
license=('EPL')
depends=('java-runtime>=7')
makedepends=('unzip')
source=("https://bintray.com/artifact/download/openhab/bin/distribution-$pkgver-designer-linux64bit.zip"
	"openhab.png"
	"openhab-designer.desktop")
noextract=("distribution-$pkgver-runtime.zip")
md5sums=('b17d19f0546a1b860d94561202102d3d'
	 '0b4767e4945ebc81123f054a13b6e8b7'
	 'c916fee3424d70e0d48163eb30517ab5')

prepare() {
	mkdir "$srcdir/openhab-designer"
	cd "$srcdir/openhab-designer"

	unzip "$srcdir/distribution-$pkgver-designer-linux64bit.zip"

}

package() {
	cd $pkgdir
	mkdir -p opt

	cp -r $srcdir/openhab-designer opt
}

