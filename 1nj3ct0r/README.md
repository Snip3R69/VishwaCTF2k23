In this question we are provided with a Wireshark Capture file named usbforensics.pcapng.

![image](https://user-images.githubusercontent.com/76834257/229893698-f8a183f6-b584-4c64-9da0-ef49e941522f.png)

It is a capture of USB protocol. Generally in a usb dump we find keyboard interrupts or
mouse clicks as user input data, so I started searching for any packet containing info
about what type of data this dump contains.

After a while I got Get Response packet of a Device:

![image](https://user-images.githubusercontent.com/76834257/229893747-8051a556-aea6-4498-9015-7622db1d015c.png)

You can see idProduct is Keyboard, by this I know this capture is storing the data of
keyboard interrupts.

Now only thing left to do is to analyse the URB_INTERRUPT IN packets particularly whose
source is 7.16.1 which is most probably device IP and destination is host.

After observing I got to know the desired packets have frame length 66, so I applied a filter
for the same:

usb.transfer_type == 0x01 and frame.len==66 and !(usb.capdata == 00:00:00:00:00:00:00:00)

![image](https://user-images.githubusercontent.com/76834257/229893877-1e0c89ee-effb-4dc6-bcd4-30d4c1b75cfe.png)

Now in every alternate packet I found HID Data:

![image](https://user-images.githubusercontent.com/76834257/229893946-9610a093-12fc-4233-a714-c3581b87687d.png)

Following this I got the whole flag:

```FLAG: VishwaCTF{n0w_y0u_423_d0n3_w17h_u58_f023n51c5}```
