# Maintainer: juankfree <juan77.sonic at gmail dot com>
pkgname=razer-blackwidow-ultimate
pkgver=0.0.5
pkgrel=1
pkgdesc="Enables M1-M5 and FN keys in Linux for the Razer BlackWidow Ultimate keyboard"
arch=('any')
url="https://github.com/juankfree/razer-blackwidow-ultimate"
license=('GPL2')
depends=('python-pyusb' 'xorg-xmodmap')
provides=('razer-blackwidow-ultimate')
conflicts=('razer-blackwidow-macro-scripts')
options=('!strip')
install="razer-blackwidow-ultimate.install"
source=('https://github.com/juankfree/razer-blackwidow-ultimate/raw/94073c2e14785ba65f638362b672c9336c7624f4/razer-blackwidow-ultimate.py'
		'https://github.com/juankfree/razer-blackwidow-ultimate/raw/94073c2e14785ba65f638362b672c9336c7624f4/razer-blackwidow-ultimate.sh'
		'https://github.com/juankfree/razer-blackwidow-ultimate/raw/94073c2e14785ba65f638362b672c9336c7624f4/99-razer-blackwidow-ultimate.rules'
		'https://github.com/juankfree/razer-blackwidow-ultimate/raw/94073c2e14785ba65f638362b672c9336c7624f4/razer-blackwidow-ultimate.desktop'
)
md5sums=('f28c9a3078c51e68fdf3478aaa26ab34' '6ba8808c6c2a18b25384ccae32167cba' '09e8031d8cabdefb2d312f13d7b85357' '5214cf77dad445f191683e0705941831')
package() {
	install -Dm755 "${srcdir}/razer-blackwidow-ultimate.py" "${pkgdir}/usr/bin/razer-blackwidow-ultimate.py"
	install -Dm755 "${srcdir}/razer-blackwidow-ultimate.sh" "${pkgdir}/usr/bin/razer-blackwidow-ultimate"
	install -Dm644 "${srcdir}/99-razer-blackwidow-ultimate.rules" "${pkgdir}/usr/lib/udev/rules.d/99-razer-blackwidow-ultimate.rules"
	install -Dm644 "${srcdir}/razer-blackwidow-ultimate.desktop" "${pkgdir}/etc/xdg/autostart/razer-blackwidow-ultimate.desktop"
}
