# Maintainer: Matthew Phillip Cooper <coopertronics@gmail.com>
# Ex-Maintainer: ktamp <ktamp@chem.uoa.gr>

pkgname=sword25
pkgver=1.0
pkgrel=1
pkgdesc='Broken Sword 2.5: The Return of the Templars is a graphical point-and-click adventure game based on the classic series by Revolution Software. Take on the role of George Stobart and try to figure out what is going on.'
arch=('any')
url="http://www.brokensword25.com/"
gmpkgurl="http://downloads.sourceforge.net/scummvm/"
license=('custom')
depends=('scummvm')
source=("$gmpkgurl$pkgname-v$pkgver.zip"
  "$pkgname.sh"
  "org.$pkgname.$pkgname.svg"
  "org.$pkgname.$pkgname.desktop")
md5sums=('cd1957e836e66279ad4b7ba799f022a9'
  '84848370c66827ad4d7c78905f101c27'
  '942c0a4a703e646b42518994cdd3b338'
  '4eb7f558922857ad0e64539a1c93f435')

package() {
  ##  Install documentation
  install -D -m644 $srcdir/README $pkgdir/usr/share/doc/$pkgname/README

  ##  Install licenses
  install -d $pkgdir/usr/share/licenses/$pkgname
  install -m644 $srcdir/license-* $pkgdir/usr/share/licenses/$pkgname/

  ##  Install binaries
  install -D -m644 $srcdir/data.b25c $pkgdir/usr/share/$pkgname/data.b25c
  install -D -m755 $pkgname.sh $pkgdir/usr/bin/$pkgname

  ##  Install game icon
  install -d $pkgdir/usr/share/icons/hicolor/scalable/apps
  install -D -m644 org.$pkgname.$pkgname.svg $pkgdir/usr/share/icons/hicolor/scalable/apps/org.$pkgname.$pkgname.svg

  ##  Install Application desktop launcher
  install -d $pkgdir/usr/share/applications
  install -D -m644 org.$pkgname.$pkgname.desktop $pkgdir/usr/share/applications/org.$pkgname.$pkgname.desktop
}
