# Maintainer: h
# Contributor: h
pkgname=hoffice-bin
pkgver=11.20.0.1520
pkgrel=1
pkgdesc="Office document editor for Linux. Hancom Office Editor is an application to allow you to edit office documents that is developed and distributed by Hancom Inc."
arch=('i686' 'x86_64')
url="http://www.hancom.com"
license=('custom')
groups=('hoffice')
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
	'nimf'
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
source=("https://cdn.hancom.com/pds/hnc/DOWN/gooroom/hoffice_${pkgver}_amd64.deb"
        'hoffice-bin.install')
sha256sums=('1ecb2f82e915b49706d1f5f6d206f8bd4a9384fda2bd56798c94046865fe5730'
            '61e6ec4ba788add38aa6fb1ad8229c747177daca1df381943bb4ceae710e8054')

DLAGENTS=('https::/usr/bin/curl -fLC - --retry 3 --retry-delay 3 -e https://www.hancom.com/cs_center -o %o %u'
          "${DLAGENTS[@]}")

package() {
	# Extract package data
	ar x "hoffice_${pkgver}_amd64.deb" ./data.tar.xz
	tar xf data.tar.xz -C "${pkgdir}"

}
