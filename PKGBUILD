# Contributor: Arch Haskell Team <arch-haskell@haskell.org>
# Package generated by cabal2arch 0.6.1
pkgname=curry-frontend
pkgrel=1
pkgver=0.2.4
pkgdesc="Compile the functional logic language Curry to several intermediate formats"
url="http://hackage.haskell.org/package/curry-frontend"
license=('custom:OtherLicense')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-cabal' 'haskell-curry-base>=0.2.2')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/curry-frontend/0.2.4/curry-frontend-0.2.4.tar.gz)
md5sums=('e8b2485164e34f02abde39705b2b6c76')
build() {
    cd ${srcdir}/curry-frontend-0.2.4
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} || return 1
    runhaskell Setup build                   || return 1
    runhaskell Setup copy --destdir=${pkgdir} || return 1
    install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/$pkgname/LICENSE || return 1
    rm -f ${pkgdir}/usr/share/doc/${pkgname}/LICENSE
}
