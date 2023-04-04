Description:
My friend sent me a clip and I found it to be very interesting. I wanted to watch the
full video but before I could rewatch the clip, he deleted it!! All I have right now is
this image he sent me afterwards. Can you help me find the video link?

This question starts with a jpg file, starting with some basic analysis, everytime I
got this string in License of the image which kept on bugging me, also while
analysing common passwords of this file I got few terms like,

AAA-7Z-EC32-D32, chevalo reviens and Klemou Was Here

Also, when I tried decoding that string I got in license

IFAUCLJXLIWUKQZTGIWUIMZS

I found out it was a Base-32 decoded plain text which luckily decoded to again this,

AAA-7Z-EC32-D32

After this, I was sure it is some password to steghide or something!!

I tried steghide with this password and got a secret.zip file which had two images,

![image](https://user-images.githubusercontent.com/76834257/229894339-c5d60c21-bda8-44c3-9e44-40ec8b242e82.png)

Finally, the question itself gives a hint “XOR”

gmic n1.png n2.png -blend xor -o result.png

I used this command to XOR both the images and it resulted the FLAG

![image](https://user-images.githubusercontent.com/76834257/229894430-fec5ab6e-481f-4087-9fae-292d72981955.png)

```FLAG: VishwaCTF{https://youtu.be/LlhKZaQk860}```
