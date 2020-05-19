# pi-zero-wallet

Goals - this is an attempt to create an air-gapped cold-wallet on a pi-zero running Electrum 3.x, with the air-gap being bridged by an e-ink screen to display qr-codes and a camera to read qr-codes, along with the 4 buttons included in the e-ink HAT screen. Next stage might involve adding a num-pad in order to enter in PIN numbers. For the short-term "password" will be read-in as qr-code. 

One thing that is not in-scope for this project, unless someone wants to design one, is a pi-zero case which gracefully includes the camera, the screen and an enclosure.

Unlike some other guides, I'm not going to fanatical about keeping the pi off-line during setup, but the goal is for it to be off-line post-setup indefinitely. It's main purpose would be holding the master private key, while still allowing signing of transactions via the qr mechanism.

First follow steps outlined here for access to pi zero without having to plugin KVM
https://desertbot.io/blog/headless-pi-zero-ssh-access-over-usb-windows

1. ~~connect from SSH via ethernet over usb~~
2. install wallet software
    - attempt to read/sign/write transaction via USB file transfer
3. install camera
   - attempt to activate camera, take picture
   - attempt to read a QR code
4. install eink screen
   - attempt to display any image
   - attempt to display QR code from file that can be read from phone
   - attempt to read buttons and do something with them
5. write a program
- accepts command from button
- inputs a QR codes transaction
- sends it to wallet for signing
- signs it and returns either a string or QR code image
- either QR encodes the string or displays the QR code image

future:
 - lock/unlock with buttons
 
4 buttons:
- all buttons unlock - locks after timeout
- share master public key
- sign transaction
- lock

