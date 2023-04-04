In the question we are provided with a file with “Extension Error” after checking its
header file, It was really clear it is a GIF file.

![image](https://user-images.githubusercontent.com/76834257/229889683-af7e9645-3268-42b9-b626-d594c20a747f.png)

Converting this file to GIF will show result like this,

![image](https://user-images.githubusercontent.com/76834257/229889791-f30ddbbf-6cb4-4392-9f50-ddf90b4bfc8e.png)

After checking some data related to this GIF like strings, frames, and steghide I checked

its metadata and got a string in comments which was in base64 format.

dmlzaHdhQ1RGe3ByMDczYzdfdXJfM1gxRn0=

Decrypting this to plain text got me to the Flag.

```FLAG: vishwaCTF{pr073c7_ur_3X1F}```
