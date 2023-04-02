We were given a web server with login page. And a button which showed me the source code of the site. There was a thing strcmp() which expected value to be 1. 

First I tried out some SQL injection payloads from https://github.com/payloadbox/sql-injection-payload-list and one of the payload gave me an error saying strcmp() is set to be 1

This made me kind of confused so I decided to do a bit research on it and found an article https://www.doyler.net/security-not-included/bypassing-php-strcmp-abctf2016

So I tried the way he did by making ?username[]=""&password[]="" but its was still throwing out the same issue. Then i decided to do a few more research and found out that the above article was for solving the strcmp() value to be set 0 and my error showed it to make me 1 so I tried to search upon how to make it 1 and not 0 and tried playing with the URL for a while and when i made the url ?username=admin&password[]="" I saw the same error again Until i checked down below the password box the flag laying xD
