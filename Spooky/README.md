This challenge was a bit tricky

This challenge had a login page as well. So firstly I tried out some SQLi payloads but of no use.

So the next step I took was dirsearch where i found out 2 direcories showing 200 status login.php and sitemap.xml

Login.php had nothing at that time so I followed to visit sitemap.xml where i found 2 more hidden directories /creds/users.txt and /creds/pass.txt.

So it was again the time for bruteforce. I used hydra thc here with command "hydra -L users.txt -P pass.txt <server> http-post-form "/login.php:user=^USER^&pass=^PASS^:Invalid username or password!!'"
But somehow it was showing me a bit error so i tried bruteforcing it with 1 by 1 usernames.
  
  And then ```shrekop``` was the user who had the pass VM something from pass.txt
  
  I thought I had won until I logged in as shrekop to be just a "(USER)" :(
  
  Now the this hints me that yup we need to escalate user to admin somehow and for that i tried few a lot things starting from putting inspecting all the headers if there is any possible way to make me admin. Looked upon if there exists any cookie but nope.
  
  Then I thought of using a bit params and tried putting in /login.php?admin=1 and ?/login.php?admin=true but it didnt work as well.
  
  I thought maybe there'l be a custom header and I tried adding Admin: 1 and Admin: true into the burp but again of no use.
  
  Almost given up I thought of using the same concept into the below given field where it mentioned user=shrekop&pass=blabla
  
  So I used and extra param here &admin=1 it didnt work and finally the almighty param &admin=true and BOOM it worked :D. That was a really great chall tbh.
  
![image](https://user-images.githubusercontent.com/76834257/229354725-f4e37328-6aa0-4b97-a816-0d1f4f503ee9.png)
