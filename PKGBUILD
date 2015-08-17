# Maintainer: Christian Zucchelli (@Chris_Zeta) <thewebcha@gmail.com>
pkgname=sgit
pkgver=20120327
pkgrel=5.51
pkgdesc="Git gui from a shell"
arch=('any')
url="https://github.com/ChrisZeta/SGit/"
license=('GPL')
depends=('git')
provides=('sgit')


_gitname=SGit
_gitroot='git://github.com/ChrisZeta/SGit.git'


build() {
  cd $srcdir

  msg "Connecting to GIT server...."
  
  if [[ -d $_gitname ]]; then
    cd $_gitname || return 1
    git pull || return 1
  else
    git clone $_gitroot || return 1
  fi
  msg " checkout done."
  
  cd $srcdir/$_gitname/src || return 1
    
  install -Dm755 SGit.sh "${pkgdir}/usr/bin/sgit"
 }



# vim:set ts=2 sw=2 et:
