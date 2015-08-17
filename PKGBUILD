# Maintainer: shmilee <echo c2htaWxlZS56anVAZ21haWwuY29tCg==|base64 -d>

pkgname=weicoair
pkgver=1.54
pkgrel=3
pkgdesc="A clear Sina Weibo client based on Adobe AIR."
arch=('i686' 'x86_64')
url="http://www.eicodesign.com/weico/air.html"
license=(custom)
if [[ "${CARCH}" == 'x86_64' ]];then
  depends=('adobe-air' 'lib32-libxt' 'lib32-libxslt' 'lib32-libxtst')
else
  depends=('adobe-air' 'libxt' 'libxslt' 'libxtst')
fi
source=('http://static.weico.s3.sinaapp.com/WeicoAir.zip' 'weicoair.desktop' 'weicoair' 'icon.png')
md5sums=('8c207aca743bb596e532088292e161d9' 'a222a1ddf8d34112b880cb37fbebefcd' '626f4c9fe0537a0379f943177a429513' 'a752b5bbee0085a06ce04b5c5b1ee308')
package()
{
  cd ${srcdir}
  install -d ${pkgdir}/{usr/share/applications,usr/bin,opt/${pkgname}}

  install -Dm644 weicoair.air ${pkgdir}/opt/${pkgname}/
  install -Dm644 icon.png ${pkgdir}/opt/${pkgname}/

  install -Dm644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/
  install -Dm755 ${pkgname} ${pkgdir}/usr/bin/${pkgname}
}
