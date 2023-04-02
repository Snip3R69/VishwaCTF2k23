### ```FIRST BLOOD```

![image](https://user-images.githubusercontent.com/76834257/229356309-9bd91f1b-6fac-47d3-a589-06199c68d35c.png)

### Super32 gotta be my favourite gender :)
This was one of the best ever challenges I have ever solved to be honest.

So lets begin

## DESCRIPTION
The challenge is all about surfing the internet.

And a .txt file named ```httpsyoutube.com@jee_engineering.txt```

## Solution

So firstly ezpz I visited the @jee_engineering yt channel as mentioned on the txt file name (also to mention the text file was empty).
![image](https://user-images.githubusercontent.com/76834257/229356440-f75c4b62-3b91-4d4a-a9be-4e152aa43b56.png)

Firstly I saw that it had a single video uploaded on it where he clutched in Valo :) Also commented down below hehe. I was just tryna check if there is anything inside the video or comments but found nothing and coming forward the about section of this channel had some hints:
![image](https://user-images.githubusercontent.com/76834257/229360278-01a5c8bd-48ce-44d4-9fc1-fc1fc02ff14a.png)

First I went forward looking for who is hosting the jee advanced for this year 2k23 and found the wikipedia with whole table of details with it:
![image](https://user-images.githubusercontent.com/76834257/229360377-47bf260f-0dc1-43c3-936d-2cf0ffececa5.png)

As it says IIT Guwahati is gonna host this years advanced paper I went forward to check their twitter for a brochure as mentioned in the yt about section and found a post:

![image](https://user-images.githubusercontent.com/76834257/229360455-6a79fad8-e63a-4250-b514-43b55b2c73c9.png)

Also mentioned in the about section of YT to check quoted retweets when we open it we just find a single quoted retweet:
![image](https://user-images.githubusercontent.com/76834257/229360557-f1719059-0605-454e-b7b2-8eabdd777e23.png)

Again the tweet here mentioned JEE Advanced chemisty paper and an Instagram handle, So i tried to lookup for an insta handle with same username and I was successful finding such and account with a single post:

![image](https://user-images.githubusercontent.com/76834257/229365792-881e6084-3b31-4e6a-81b1-3c8a388ce3aa.png)

Now as we see in the comment again there is mentioned about the chemmisty paper hosted by IIT Guwahati itself last time and upon the same wikipedia we can see it was hosted back in 2016, well that comes later, we can even find a mention of a github account with a repo but the username has 1 in its username so accordingly i searched for the same on github and found this:

![image](https://user-images.githubusercontent.com/76834257/229365937-65a9e144-eb4a-4739-915c-e172dc3446be.png)
 
 and upon opening the repo was some chinese font which when translated says: 
 
 ![image](https://user-images.githubusercontent.com/76834257/229365984-63971f18-100f-4504-99c8-b6cb0761e086.png)

Also above we can see that there are 5 commits which when i viewed, I found out a .cpt file. First I was confused what a cpt file is and upon research I found an article buy redhat upon txt file encryption and decryption by a tool named ```ccrypt```

So I simply donwloaded the file on my linux machine and used the decrypt command 
```
ccdecrypt flag.txt.cpt
```
upon which it asked me for a decryption key. At first I was confused then I remebered about the mention of chem paper so I searched for jee advance 2016 papers which were in 2 sections but there were 5 Integer type questions as mentioned in the insta comment so I scrolled to the integer type questions and then as the repo said i interlinked the answers respectively ```94655```

And BOOM

![image](https://user-images.githubusercontent.com/76834257/229366235-b6defa2f-448f-4359-995c-f22655ef6050.png)


Again the flag wasm't direct it asked for the password of that file to be input upon the flag too so finally the flag became:

### ```VishwaCTF{11T_9UW4HAT1_2023_94655}```
