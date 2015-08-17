# Maintainer: Antoine Lubineau <antoine@lubignon.info>

pkgname=picviz-gui
pkgver=0.7
pkgrel=3
pkgdesc="A parallel coordinates plotter which enables easy scripting from various input (GUI)"
arch=('any')
url="http://www.wallinfire.net/picviz/"
license=('GPL')
depends=('libpicviz' 'python2-qt')
options=(!strip)
source=("http://www.wallinfire.net/files/picviz/$pkgname-$pkgver.tar.gz"
        'picviz-gui.desktop')
md5sums=('86f28498d5ae77d070542b5e2f241a90'
         '73c81fc6c62261d923ddd3d33dfee637')

package() {
  install -D -m 0644 picviz-gui.desktop "$pkgdir/usr/share/applications/picviz-gui.desktop"

  cd "$srcdir/$pkgname-$pkgver"
  python2 setup.py install --root="$pkgdir/" --optimize=1
}

# vim:set ts=2 sw=2 et:
