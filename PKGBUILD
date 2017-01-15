pkgname=referenceassemblies-pcl
pkgver=4.6
pkgrel=1
pkgdesc='Microsoft .NET Portable Library Reference Assemblies'
arch=('x86_64')
license=('custom')
url="http://www.microsoft.com/en-us/download/details.aspx?id=40727"
depends=('mono')
makedepends=('git')
_commit='874cf94eeaf35aa267878f9983b280a00e7bed19'
source=("git+https://github.com/directhex/xamarin-referenceassemblies-pcl#commit=${_commit}"
        'https://github.com/directhex/xamarin-referenceassemblies-pcl/raw/centos/EULA.rtf')
sha256sums=('SKIP'
            '9643c50ddbc7545b873265457a9662fb2da104db800315c3141f04364717b91e')

package() {
  cd xamarin-referenceassemblies-pcl

  install -dm 755 "${pkgdir}"/usr/lib/mono/xbuild-frameworks/.NETPortable/
  cp -dr --no-preserve='ownership' v4.{0,5,6} "${pkgdir}"/usr/lib/mono/xbuild-frameworks/.NETPortable/

  install -Dm 644 ../EULA.rtf -t "${pkgdir}"/usr/share/licenses/referenceassemblies-pcl/
}

# vim: ts=2 sw=2 et:
