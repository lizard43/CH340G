# CH340G
Some Arduino clones use a CH340G USB chip and you'll need to install a driver

The zip files are from the vendor site.
The Windows seems to work ~ok.
Don't have a Mac, can't vouch for that driver.
The Linux driver as-is only support 3.9 or less kernel versions

In order to support 3.9+ kermels, the ch34x.c file needed to be edited. This change is in the ch340g folder.
The old, original file for ref is in the old340 folder

The difference is that between kernel version, they renamed the struct usb_serial_port port number field from 'number' to 'port_number'

Diff the ch34x.c files to see what I'm talking about.

To build and install just do:

make

make load
