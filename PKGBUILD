# Maintainer: Klaas Boesche <aurkagebe@gmail.com>
# Contributor: Alexandre Isoard <alexandre.isoard@gmail.com>
pkgname=i3-gnome
_pkgname=i3
pkgver=4.6
pkgrel=1
pkgdesc="Integrate the i3 window manager into GNOME"
url="http://i3wm.org/"
arch=('any')
license=('GPL')
depends=("i3-wm>=4.0" "desktop-file-utils" "gnome-session>=3.8")

install=$pkgname.install
source=("$pkgname-xsession.desktop" "$pkgname" "$pkgname-app.desktop" "$pkgname.session")
md5sums=('a3aa3619312acd889e106ae37c9fade1'
         '454b56d490d715dd169da4ba07dde95b'
         '9451925dde48cec7a0d7e6b7745b7252'
         '658021bd016cc8476c6e7ca40672a016')

package() {
  msg "Install $pkgname in xsessions"
  install -D -m 644 "$srcdir/$pkgname-xsession.desktop" \
    "$pkgdir/usr/share/xsessions/$pkgname.desktop"

  msg "Install $pkgname in gnome-session/sessions"
  install -D -m 644 "$srcdir/$pkgname.session" \
    "$pkgdir/usr/share/gnome-session/sessions/$pkgname.session"

  msg "Install $pkgname in /ush/share/applications"
  install -D -m 644 "$srcdir/$pkgname-app.desktop" \
    "$pkgdir/usr/share/applications/$pkgname.desktop"

  msg "Install $pkgname in /usr/bin"
  install -D -m 755 "$srcdir/$pkgname" \
    "$pkgdir/usr/bin/$pkgname"
}

# vim:set ts=2 sw=2 et:
