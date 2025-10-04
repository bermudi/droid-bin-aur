# Maintainer: Daniel Bermúdez <archlinux.i5beg at dabg.uk>
pkgname=droid-bin
pkgver=0.18.2
pkgrel=2
pkgdesc="Factory's development agent CLI"
arch=('x86_64' 'aarch64')
url="https://factory.ai"
license=('custom')
depends=('curl' 'xdg-utils' 'ripgrep')
provides=('droid')
conflicts=('droid')
options=('!strip')
source_x86_64=("droid::https://downloads.factory.ai/factory-cli/releases/${pkgver}/linux/x64/droid")
source_aarch64=("droid::https://downloads.factory.ai/factory-cli/releases/${pkgver}/linux/arm64/droid")
sha256sums_x86_64=('SKIP')
sha256sums_aarch64=('SKIP')

package() {
    # Install droid binary
    install -Dm755 "droid" "${pkgdir}/usr/bin/droid"
    
    # Create symlink to system ripgrep in factory bin directory
    install -dm755 "${pkgdir}/usr/lib/factory/bin"
    ln -s /usr/bin/rg "${pkgdir}/usr/lib/factory/bin/rg"
}
