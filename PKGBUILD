# Maintainer: h
# Contributor: h
pkgname=hoffice-hwp-bin
pkgver=11.20.0.989
pkgrel=1
pkgdesc="Hwp document editor for Linux. Hwp 2020 Beta is an editor that allows you to create Hwp documents easily in the Linux environment and edit them by applying various styles and formats."
arch=('i686' 'x86_64')
url="http://www.hancom.com"
license=('custom')
groups=('hoffice-hwp')
depends=(
	'cairo'
	'fontconfig'
	'freetype2'
	'glu'
	'harfbuzz'
	'harfbuzz-icu'
	'libcurl-gnutls'
	'qt5-base'
	'zlib'
	'nimf-git'
	'libhangul'
)
makedepends=(
	'binutils'
	'wget'
)
options=(
	'!strip'
	'!emptydirs'
)
install=${pkgname}.install
source=("https://cdn.hancom.com/pds/hnc/DOWN/gooroom/$(echo $groups | sed 's/-/\_/g')_2020_amd64.deb"
        'hoffice-hwp-bin.install')
sha256sums=('dc234b4d8813c39ee4686f09195b160e998fecd8798c91d7dd0548723fb999ae'
            '61e6ec4ba788add38aa6fb1ad8229c747177daca1df381943bb4ceae710e8054')

DLAGENTS=('https::/usr/bin/curl -fLC - --retry 3 --retry-delay 3 -e https://www.hancom.com/cs_center -o %o %u'
          "${DLAGENTS[@]}")

package() {
	# Extract package data
	ar x "$(echo $groups | sed 's/-/\_/g')_2020_amd64.deb" ./data.tar.xz
	tar xf data.tar.xz -C "${pkgdir}"

}
