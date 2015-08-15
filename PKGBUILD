# Maintainer: Nathan Hourt <nat.hourt@gmail.com>
_basename=gdrivefs
pkgname=$_basename-git
pkgver=1
pkgrel=1
pkgdesc="An innovative FUSE wrapper for Google Drive."
arch=(any)
url="https://github.com/dsoprea/GDriveFS"
license=('GPL')
depends=(python2 python2-argparse python-fusepy-git python2-google-api-python-client-hg python2-httplib2 python2-dateutil python2-six python2-wsgiref)
makedepends=(python2-distribute)
conflicts=($_basename)
source=("git+https://github.com/dsoprea/GDriveFS.git")
md5sums=('SKIP')

build() {
    cd "$srcdir/GDriveFS"
    python2 setup.py build
}

package() {
    cd "$srcdir/GDriveFS"
    python2 setup.py install --root="$pkgdir" --optimize=1
}
