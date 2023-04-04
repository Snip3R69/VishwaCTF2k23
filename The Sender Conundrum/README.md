DESCRIPTION
Marcus Got a Mysterious mail promising a flag if he could crack the password to the
file

We took the Zip file from the given downloads description of the challenge and I found that the zip
file is locked. 

![image](https://user-images.githubusercontent.com/76834257/229891718-c913a4e1-fe37-4a57-8008-11e8a024da29.png)

So I tried to crack the zip file using zip2john. And I saved the hashes in the zip file using the
command “zip2john unzipme.zip > zip.hashes”. Now I tried to bruteforcing the hashes file using the
rocyou.txt using the command “john –wordlist=rockyou.txt zip.hashes”. And From that I got the
password of the zip file.

![image](https://user-images.githubusercontent.com/76834257/229891862-e8691df3-27b0-4b93-958e-7f5068e0fa57.png)

After opening the zip file. I found the flag.

![image](https://user-images.githubusercontent.com/76834257/229891936-0f12070b-d8c8-4bbc-93bb-82d507600432.png)

```Flag: vishwaCTF{1d3n7i7y_7h3f7_is_n0t_4_j0k3}```
