## Dark Theme for Minimalistic rEFInd theme

This is a dark theme version of the clean and minimal theme for rEFInd by [evanpurkhiser][originalRepo].

> [rEFInd](http://www.rodsbooks.com/refind/) is an easy to use boot manager for UEFI based systems.

![rEFInd Minimalistic](https://i.imgur.com/GVfeSCe.jpg)

### Usage

 1. Locate your refind EFI directory. This is commonly `/boot/EFI/refind`
    though it will depend on where you mount your ESP and where rEFInd is
    installed. `fdisk -l` and `mount` may help.

 2. Create a folder called `themes` inside it, if it doesn't already exist

 3. Clone this repository into the `themes` directory.

 4. To enable the theme add `include themes/rEFInd-minimal-dark/theme.conf` at the end of
    `refind.conf`.

Here's an example menuentry configuration (from the screenshot)

```nginx
menuentry "Arch Linux" {
	icon /EFI/refind/themes/rEFInd-minimal/icons/os_arch.png
	loader vmlinuz-linux
	initrd initramfs-linux.img
	options "rw root=UUID=dfb2919d-ff78-48db-a8a7-23f7542c343a loglevel=3"
}

menuentry "Windows" {
	icon /EFI/refind/themes/rEFInd-minimal/icons/os_win.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}

menuentry "OSX" {
	icon /EFI/refind/themes/rEFInd-minimal/icons/os_mac.png
	loader /EFI/Apple/Boot/bootmgfw.efi
}
```

Entries that are autodetected should also show the proper icons.

### Background sizes

If you find the background looks blurry it may be due to the included wallpaper
being an incorrect resolution for your monitor. You can download the [original
high quality wallpaper][wallpaper], resize it as appropriate, convert it to a png, and replace the
`background.png`.

You can of course also choose your own background!

### Attribution

The OS icons are from [Lightness for burg][icons] by [SWOriginal][icon-author].
> Icons have been modified to match the dark theme.

The background for this fork is called [SYLK][wallpaper] which is by
[Richad Horvath][wallpaper-author] at [Unsplash][unsplash]. 

[originalRepo]: https://github.com/evanpurkhiser/rEFInd-minimal
[icons]: http://sworiginal.deviantart.com/art/Lightness-for-burg-181461810
[icon-author]: http://sworiginal.deviantart.com/
[unsplash]: https://unsplash.com/
[wallpaper]: https://unsplash.com/photos/_nWaeTF6qo0
[wallpaper-author]: https://unsplash.com/photos/_nWaeTF6qo0
