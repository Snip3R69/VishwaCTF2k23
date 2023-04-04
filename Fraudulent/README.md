Description:
I got ditched by someone and I need your help !!! The bill amount that was
charged to me was not correct. The image of the bill was corrupted. Sources said
that some PIXELS of the image were FORRENSICAllY manipulated or edited,
leading to changes in the total bill amount. You have to reach the image to see
what happened. Remember to analyze every pixel of the image carefully.
P.S.: Round off the actual total amount to closest Integer.
Flag Format : VishwaCTF{actual_total_amount}


In this question we were given a gif showing 2 frames:

![image](https://user-images.githubusercontent.com/76834257/229888191-1415bb64-05dd-4f4e-a047-069c7e39f8a6.png)

It clearly looks like a QR-code, so I tried creating one by taking 0s as White and 1s
as Black.

![image](https://user-images.githubusercontent.com/76834257/229888259-b909a020-83db-4174-a817-a96875e219a4.png)

This is the QR I made but unfortunately it didn’t work.
In the description words like manipulation, edit, analyse pixel lead me to think if there is
some manipulation
In QR , soo I tried fixing it by replacing the scanning blocks, due to pixel error, I decreased
the size of it and finally it worked!!

![image](https://user-images.githubusercontent.com/76834257/229888336-197cfc2f-e959-487a-ac84-00da7726e807.png)

Scanned this QR using this website: [QR Scanner](https://products.aspose.app/barcode/recognize)

Got this Github Repo: https://github.com/Amanjain4269/next-step.git

![image](https://user-images.githubusercontent.com/76834257/229888589-49fb16b5-5afa-4c16-bd6a-b9d6ae33780e.png)

This UseMe file had a raw data of a jpeg image converted to Base64 format.
Converted it to image file using this website:
https://codebeautify.org/base64-to-image-converter

![image](https://user-images.githubusercontent.com/76834257/229888685-7a586f21-4177-4094-820a-c1badfe1e21b.png)

It was soo obvious that this total amount won’t work, also in description it is clearly
mentioned
“The bill amount that was charged” soo I checked the Error Level Ananlysis of the image.
Website that I used: https://29a.ch/photo-forensics/#error-level-analysis

![image](https://user-images.githubusercontent.com/76834257/229888768-3037db59-7dd8-4bac-9644-9c97259d01f5.png)

You can see someone added “7” and “8” in from of the amount of Phone and Watch.

Skipping those numbers the amount lowers down to:

Phone: 23454
Watch: 6574
Laptop: 456280

Total: 486308

Tax(18%): 87535(appx.)
Final Total: 537843

This is the Original and Required amount!!

```Flag: VishwaCTF{537843}```
