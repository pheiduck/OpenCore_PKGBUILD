# Maintainer: pheiduck <pheiduck@github.com>

pkgname=opencore-efi
pkgver=0.7.0
pkgrel=32 #use the number of commits to main since this release
_mode='RELEASE'
# _mode='DEBUG'
pkgdesc='OpenCore bootloader to provide supplemental functionality for Apple-specific UEFI drivers'
url='https://github.com/acidanthera/OpenCorePkg'
_gitcommit=36869e7310637dfb2c102386841dd9b96748286a
arch=('any')
license=('BSD')
conflicts=('refind' 'clover-efi')
source=("https://github.com/acidanthera/OpenCorePkg/releases/download/$pkgver/OpenCore-$pkgver-$_mode.zip")
sha512sums=('7964a72d3264e38d0a3b805febda671b64bde8878b348b06f953d3c8930aa1e37f12b65c814be9177d5fce27eb342f5352ecd1c65f87b2c98bf1729e0200864a')

package(){
  install -d "$pkgdir/boot/EFI"
  cp -a "$srcdir/X64/EFI/OC" "$pkgdir/boot/EFI/"

  install -D "$srcdir/X64/EFI/BOOT/BOOTx64.efi" "$pkgdir/usr/lib/$pkgname/EFI/BOOT/BOOTx64.efi"

  install -d "$pkgdir/usr/share/doc"
  cp -a "$srcdir/Docs" "$pkgdir/usr/share/doc/$pkgname"
}
