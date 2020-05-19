# pi-zero-wallet

Goals - this is an attempt to create an air-gapped cold-wallet on a pi-zero running Electrum 3.x, with the air-gap being bridged by an e-ink screen to display qr-codes and a camera to read qr-codes, along with the 4 buttons included in the e-ink HAT screen. Next stage might involve adding a num-pad in order to enter in PIN numbers. For the short-term "password" will be read-in as qr-code. 

One thing that is not in-scope for this project, unless someone wants to design one, is a pi-zero case which gracefully includes the camera, the screen and an enclosure.

Unlike some other guides, I'm not going to fanatical about keeping the pi off-line during setup, but the goal is for it to be off-line post-setup indefinitely. It's main purpose would be holding the master private key, while still allowing signing of transactions via the qr mechanism.

First follow steps outlined here for access to pi zero without having to plugin KVM
https://desertbot.io/blog/headless-pi-zero-ssh-access-over-usb-windows


