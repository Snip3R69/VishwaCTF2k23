1. Aperisolve, stegonline did not yield any results except for a password.

![image](https://user-images.githubusercontent.com/76834257/229896445-c98f702a-fd00-455d-93c1-20f3a17009ad.png)

2. Password did not work with the original image in steghide.

3. opened image in hexeditor, saw extra data after file trailer ffd9

![image](https://user-images.githubusercontent.com/76834257/229896577-c7151779-0a82-473d-b85e-322888df5641.png)

4. copied that data into another file

5. Opened that file as an archive and extracted it

6. A thousand images available.

![image](https://user-images.githubusercontent.com/76834257/229896718-d45114e1-6384-4674-9356-3955a1944a21.png)

7. Brute forced all of them with the password. Got the flag.

```
import subprocess
impath = r"C:/Users/%USER%/Desktop/RitSec CTF/cid/CID HQ/"
data = []
dataImages = []
for i in range(369, 370):
try:
print(subprocess.check_output(["steghide", "extract", "-sf", impath + f"{i}.jpg", "-p",
daya darwaza tod do"]))
dataImages.append(i)
data.append(subprocess.check_output(["steghide", "extract", "-sf", impath +
f"{i}.jpg", "-p", "daya darwaza tod do"]))
except subprocess.CalledProcessError as e:
print("Failed image number ", i)
print("\n\n")
print(data)
print("\n\n")
print(dataImages)
```
