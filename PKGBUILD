# Maintainer: Alucryd <alucryd at gmail dot com>

pkgname=ruby-iconv
pkgver=1.0.3
pkgrel=1
pkgdesc="Wrapper library for iconv"
arch=('any')
url="https://github.com/nurse/iconv"
license=('GPL3')
depends=('ruby')
makedepends=('rubygems')
source=("https://rubygems.org/downloads/${pkgname#*-}-${pkgver}.gem")
sha256sums=('94a9b62a56c96226b62b787cd45fdc48c03f4517f1e36e64db113b010fb012da')

package() {
  cd "${srcdir}"

# Install GEM
  local _gemdir="$(ruby -rubygems -e 'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}"${_gemdir} ${pkgname#*-}-${pkgver}.gem
}

# vim: ts=2 sw=2 et:
