# Maintainer: pheiduck <pheiduck@github.com>

pkgname=opencore-efi
pkgver=0.7.1
pkgrel=0 #use the number of commits to main since this release
_mode='RELEASE'
# _mode='DEBUG'
pkgdesc='OpenCore bootloader to provide supplemental functionality for Apple-specific UEFI drivers'
url='https://github.com/acidanthera/OpenCorePkg'
_gitcommit=be2d9fe75a29b682441ca69dfbb87068258b42f5
arch=('any')
license=('BSD')
conflicts=('refind' 'clover-efi')
source=("https://github.com/acidanthera/OpenCorePkg/releases/download/$pkgver/OpenCore-$pkgver-$_mode.zip")
sha512sums=('0191666f246db54787cb73685e779c8c60b42fd4924103304323f9e1b973fd7050b9030dcd3b5d9b9fdb4399b2d7197f383a1aefe9f2f32ddc3ccd5147472cba')

package(){
  install -d "$pkgdir/boot/EFI"
  cp -a "$srcdir/X64/EFI/OC" "$pkgdir/boot/EFI/"

  install -D "$srcdir/X64/EFI/BOOT/BOOTx64.efi" "$pkgdir/usr/lib/$pkgname/EFI/BOOT/BOOTx64.efi"

  install -d "$pkgdir/usr/share/doc"
  cp -a "$srcdir/Docs" "$pkgdir/usr/share/doc/$pkgname"
}
