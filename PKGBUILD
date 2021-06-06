# Maintainer: pheiduck <pheiduck@github.com>

pkgname=opencore-efi
pkgver=0.6.9
pkgrel=79 #use the number of commits to main since this release
_mode='RELEASE'
# _mode='DEBUG'
pkgdesc='OpenCore bootloader to provide supplemental functionality for Apple-specific UEFI drivers'
url='https://github.com/acidanthera/OpenCorePkg'
_gitcommit=b498683dcf58a508d7818cb76d256b4a83202440
arch=('any')
license=('BSD')
conflicts=('refind' 'clover-efi')
source=("https://github.com/acidanthera/OpenCorePkg/releases/download/$pkgver/OpenCore-$pkgver-$_mode.zip")
sha512sums=('5cf969912e3643c1ff9614ef2d453cf851ece2bf0324dc58e432338acbde1197f671b17636c7a4ae370086d1b02b1449060765b5a27a38975883cbe50b3d3ab5')

package(){
  install -d "$pkgdir/boot/EFI"
  cp -a "$srcdir/X64/EFI/OC" "$pkgdir/boot/EFI/"

  install -D "$srcdir/X64/EFI/BOOT/BOOTx64.efi" "$pkgdir/usr/lib/$pkgname/EFI/BOOT/BOOTx64.efi"

  install -d "$pkgdir/usr/share/doc"
  cp -a "$srcdir/Docs" "$pkgdir/usr/share/doc/$pkgname"
}
