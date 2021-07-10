# Contributor: speps <speps at aut dot archlinux dot org>
# Contributor: Reihar <reihar at necronomicon dot fr> 

pkgname=plowshare-git
pkgver=2.1.7.r3.g593a60ae
pkgrel=1
pkgdesc="Command-line downloader and uploader for Rapidshare, Mediafire and other file sharing websites."
arch=('any')
url="https://github.com/mcrapet/plowshare"
license=('GPL3')
depends=('curl' 'js78' 'recode')
makedepends=('git')
optdepends=('bash-completion: enable bash auto completion'
            'imagemagick: X11 picture viewer for captchas'
            'sxiv: X11 picture viewer for captchas'
            'feh: X11 picture viewer for captchas'
            'qiv: X11 picture viewer for captchas'
            'fbida: framebuffer picture viewer for captchas'
            'libcaca: framebuffer ascii picture viewer for captchas')
provides=('plowshare')
conflicts=('plowshare')
replaces=('plowshare-svn')
source=("$pkgname::git+https://github.com/mcrapet/plowshare.git")
md5sums=('SKIP')

pkgver() {
  cd $pkgname
  git describe --long --tags | sed 's/.//;s/-/.r/;s/-/./'
}

package() {
  cd $pkgname
  make install DESTDIR="${pkgdir}/" PREFIX=/usr
}

# vim:set ts=2 sw=2 et:
