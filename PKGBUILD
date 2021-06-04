# Maintainer: pheiduck <pheiduck@github.com>

pkgname=opencore-efi
pkgver=0.6.9.r0.g3d15506
pkgrel=76 #use the number of commits to main since this release
_mode='RELEASE'
# _mode='DEBUG'
pkgdesc='OpenCore bootloader to provide supplemental functionality for Apple-specific UEFI drivers'
url='https://github.com/acidanthera/OpenCorePkg'
_commit='3d15506a33a60a492adbb1ea8ed803a055c49aea'
arch=('any')
license=('BSD')
conflicts=('refind' 'clover-efi')
source=("https://github.com/acidanthera/OpenCorePkg.git#commit=$_commit")
sha512sums=('SKIP')

package(){
  install -d "$pkgdir/boot/EFI"
  cp -a "$srcdir/X64/EFI/OC" "$pkgdir/boot/EFI/"

  install -D "$srcdir/X64/EFI/BOOT/BOOTx64.efi" "$pkgdir/usr/lib/$pkgname/EFI/BOOT/BOOTx64.efi"

  install -d "$pkgdir/usr/share/doc"
  cp -a "$srcdir/Docs" "$pkgdir/usr/share/doc/$pkgname"
}
