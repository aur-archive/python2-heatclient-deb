# Maintainer: James Bulmer <nekinie@gmail.com>

pkgname="python2-heatclient-deb"
pkgver=0.2.8
pkgrel=2
pkgdesc="Client library for Openstack"
arch=("i686" "x86_64")
url="http://docs.openstack.org/developer/python-heatclient/"
license=("Apache")

depends=(
  "python2"
  "python2-pbr"
  "python2-iso8601"
  "python2-prettytable"
  "python2-keystoneclient"
  "python2-six"
  "python2-requests"
)

makedepends=("python2-setuptools")
conflicts=("python2-heatclient" "python2-heatclient-git")
source=("http://archive.ubuntu.com/ubuntu/pool/main/p/python-heatclient/python-heatclient_${pkgver}.orig.tar.gz")
md5sums=("32749bd0c5f97d4165fb4f215133fc1b")

build() {
  cd "${srcdir}/python-heatclient-${pkgver}/"
  python2 setup.py build
}

package() {
  cd "${srcdir}/python-heatclient-${pkgver}/"
  python2 setup.py install --root="${pkgdir}/" --optimize=1
}