We were given a button on the webserver which when pressed gave me the info about the system details.

So again dirsearch found robots.txt on the website which when accessed gave me the source code having if else condition mentioning cmd and btn.

So as we press the system details button we see that in the url /?btn= appears so simply i changed btn to cmd and to check for if the commands work i tried ?cmd=ls

and boom it gave me the files inside the directory index.html, index.php and one more file forgot the name. So i simply used command ?cmd=cat+index.php

to notice i wasnt getting the flag anywhere instead the site was getting rendered so I decided to use an alt for cat command and i did the changes ?cmd=tac index.php

and there we go, i found the whole source code with the flag.

![WhatsApp Image 2023-04-02 at 18 18 08](https://user-images.githubusercontent.com/76834257/229353786-d4adc0b6-9c26-4d13-b25a-23461155583b.jpg)

Dont mind my photo i put it on my story to show people i am resuming back on ctf ofc with the flag and url blurred out @snip3r.gg ;)
