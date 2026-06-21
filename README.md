# Computer Networks

## why do we need layers?
### ***Ans-***
**Sending a message from your phone to a friend's phone**

### **many tasks happen**
- **converting data into signals**
- **sending through cables/wifi**
- **finding the destination**
- **checking errors**
- **delivering to the correct application**

**Instead of one huge protocol doing everything networking divides responsibilities into layers**

**each layer perform a specific job and communicate with the layer above and below it**

## OSI Model (7 layers)
### ***Too -> bottom***
| Number | Layer | Protocol |
|-------|-------|----------|
| 7 | Application | Provides network services to users |
|  6 | Presentation | Data format , encryption,compression|
| 5 | Session | Manges communication sessions|
| 4 | Transport | Reliable delivery,Flow control |
| 3 | Network | Routing and IP addressing |
| 2 | Data Link | MAC addressing, error detection |
| 1 | Physical | Transmits bits over medium |

### ***7. Application Layer***
**This is where user applications work**

***Examples-***
<br>
**Browser,Gmail,whatsApp,FTP cliet etc**
<br>
***Protocols-***
<br>
**HTTP,HTTPSFTP,SMTP,DNS**

### ***6. Presentation Layer***
***Responsible for***
<br>
- **encryption**
- **compression**
- **Data translation**

***Examples-***
<br>
**HTTPS encryption,JPEG image formation**

### ***5. Session  Layer***
**Responsible for-**
<br>
- **Establish session**
- **Maintain  session**
- **Terminate session**


**Fuctions-**
<br>
- **Dialog control (whose turn to send)**
- **Token management**
- **Synchronization /  checkPoint**

***Examples-***
<br>
**During a vedio call , the session layer helps maintain the communication session**

***Note - Session layer manages , establishes nad terminates communication sessions between two device***

### ***4. Transport Lyaer***
**Provides end to end communication**
<br>
***Protocols-***
<br>
**Reliability,Flow control , error recovery**
<br>
***Examples-***
<br>
**when downloading a pdf , TCP ensures all data arrives correctly**

### ***3. Networking Layer***
***Main job-*** **Routing packets**
<br>
***Protocol-*** **IP**
<br>
***Device-*** **Router**
<br>
***Examples-***
<br>
**Finding the best path from BBSR to Bangalore**

### ***2. Data Link Layer***
***Responsible for-***
<br>
**MAC address , framing,Error detecting**
<br>
***device-*** **switch**
<br>
***Examples-***
<br>
**communication inside the same LAN**

### ***1. Phisical Layer***
**Lowest Layer**
<br>
***Responsible for-***
<br>
**sending 0s and 1s**
<br>
***Examples-***
<br>
**ethernet cable , fiber optic cable , Radio signals**
<br>
***Devices-*** **Hub,Repeater**

|TCP/IP Layers | OSI Layers |
|--------------|------------|
|Application|Application + Presentation + Session|
|Transport|transport|
|Internet|Network|
|Link|Data Link|
|Physical|Physical|

### Difference

|OSI|TCP/IP|
|----|------|
|7 layers|4/5 layers|
|Reference model|Practical model|
|Devloped by ISO|Devloped by DOD|


## Transport Services Avaliable to Applications

- **Reliable Data Transfer**
- **Throughput**
- **Timing**
- **Security**

### ***1. Reliable Data Transfer***
**Data should reach the destination**
- **without loss**
- **without duplication**
- **in correct order**

***Examples-***
<br>
**sending bank transaction , Resume upload, Email must be reliable.
Therefore these use TCP.**

### ***2. Throughput***
**Amount of data transfered per second**
<br>
**Measured in bps , kbps,mbps,gbps**

***Exaamples-***
<br>
**100 MB file in 10sec so 10MB/sec**
<br>
**Higher Throughput = Faster Transfer**

### ***3. Timing***

**Data Should arrive on time**

***Examples-*** **Video Call**
<br>
**If your friend's voice reaches after 20sec conversation becomes impossible**
<br>
**Timing is more important than perfect reliability here**
<br>

***Applications-***
<br>
**Zoom,Google meet,Online Gaming**

### ***4. Security***
**Protect data from attackers**

***Examples-***
<br>
**While entering(Password,ATM pin) data must be encrypted**
**HTTPS provides this**

## **TCP Services**
**TCP -** ***Transmission Control Protocol***
<br>

**2 Major Services :**
- **Connection - Oriental Service**
- **Reliable Data Transfer**

### ***Connection - Oriented Service***
**Before sending data, TCP establishes a connection. This is called the 3-way handshake**
```text
Client - SYN
Server - SYN + ACK
Client - ACK
```
**Connection Establish**

### ***Reliable Data Transfer***
**TCP guarantes No loss , No duplication , Correct Order**

***Examples -***
<br>
**Pockets sent: 1 , 2, 3, 4 . if packet 3 is lost TCP notices and retransmit and recieve : 1 , 2, 3 ,4**

### ***Full Duplex***
**Both sides can send and recieve simultaneously.**

***Examples -*** **Phone Call**
<br>
**You speak and listen together not like walkie - talkie**

### ***TCP Congestion Control***
**Congestion = too much traffic**

***Examples -***
<br>
**Imagine a highway**
<br>
**Normally : 100 Cars**
<br>
**Trafic flows smoothly**
<br>
**Suddenly : 10000 cars**
<br>
**Trafic jam occurs**
<br>
**Similarity networks become congested TCP automatically slows transmission . This is called congestion control**

## **UDP Services**
**UDP -** ***User Datagram Protocol*** 
- **Connectionless**
- **Unreliable**
- **No Congestion Control**

### ***Connectionless***
**No Handshake**

***Examples -***
<br>
**Sending a letter. Simply drop it in the mailbox.No confirmation first.**

### ***Unreliable***
**UDP does not care if packets are lost**

***Examples -*** **Voice Call**
<br>
**Suppose one voice call packet is lost . Instead of ```Hello..```
we have ```He...lo```**
<br>
**Waiting for retransmission wuld create delay .So UDP avoit it.**

### ***NO ordering Guarante***
```
Send : 1,2,3,4
Recived : 2,1,4,3
```
**UDP does not fix this**

### ***No Congestion Control***
**UDP keeps sending**

***Examples -***
<br>
**Imagine a person throwing ball continuously even if reciever is overloaded**

***Why Use UDP?***
- **Faster**
- **Less overhead**
- **Lower delay(less latency)**
<br>

**Applications - Video call,Live streaming,Online Games,DNS**

### ***TCP VS UDP***
|TCP|UDP|
|---|---|
|Connection Oriented|Connectionless|
|Reliable|Unreliable|
|Ordered Delivery|No Ordering Gurantee|
|Congestion Control| No Congestion Control|
|Slower|Faster|
|Used HTTP,HTTPS,FTP|Used DNS, Gaming Streaming|

## **Application Layer**

### ***HTTP - Hyper Text Transfer Protocol***
**It is protocol used for communication between web Browser(Client) and Server.**

***Example-***
<br>
**Enter :**
**```www.amazon.com```**
<br>
**Browser Says :**
```Please give me the home page```
<br>
**Server Replys :**
```Here is the home page (HTML,CSS and some Images)```

### ***HTTP used TCP*** 
**Website does not afford missing data . so HTTP needs Reliability. It uses TCP.**

### ***HTTP uses PORT number 80***

***Othere Examples-***
```
80 -> HTTP
443 -> HTTPS
21 -> FTP
25 -> SMTP
```
**PORT like a door when HTTP trafic arrives, it usually enters through door 80.**

### ***HTTP is Stateless***

**Stateless means - Server does not remember previous request. Treat each request as fresh**

***Example-***
<br>
**Request1**
```
Client : Give me page number 1
Server : Here is Page number 1
```
**server forgets**
<br>
**Request2**
```
Client : Gime me page number 2
Server : Here is Page number 2
```
**Server treat this msg as completely new message**

***NOTE-***
<br>
**Suppose visit ```amazon.com``` and add some product to card then if HTTP is stateless how Amazon remember the cart products ?**
<br>

***ANS-*** **Cookies and sessions**
### ***Client Server Architecture***
***Client  -*** **Web Browser, Mobile App**
<br>
***Server  -*** **Google Server,AmazonServer** 
```
Client ---Request---> Server
Client <---Resposne--- Server
```

### ***HTTP Request Example***
```
GET /somedir/page.html HTTP/1.1
Host: www.someschool.edu
Connection: close
User-agent: Mozilla/5.0
Accept-language: fr
```
***Explanation***
<br>
**Code :**
```
GET/page.html
```
**Means :**
```
Please send me page.html
```
**Code :**
```
HOST: www.example.com
```
**Tells the server :**
```
Which website trying to access
```
**May be one server host multiple websites**
<br>
**Code :**
```
User-agent: Chrome
```
**Tells the server :**
```
I am Chrome Browser
```
**Code :**
```
Accept-language: fr
```
**Means :**
```
I prefer french language
```
**Server may send content accordingly**

### ***HTTP Response Message***
```
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 6821
```
**Code :**
```
HTTP/ 200 OK
```
**Means :**
```
Request successful
```
**Code :**
```
Content-Type: text/html
```
**Means :**
```
I am sending HTML data
```
**Other Examples :**
```
image/png
application/pdf
video/mp4
```
**Code :**
```
Content-Length: 6821
```
**Menas :**
```
Response size is 6821 bytes
```

### ***Other HTTP Responses***

***200 OK -*** **Everything worked and website found**
<br>
***301 Moved Permanently -*** **Page has been shifted. from old website redirect to new website**
<br>
***400 Bad request*** - **Request format is wrong**
<br>
***404 Not found*** - **Request page does not exist**
<br>
***500 HTTP version does not Supported -*** **Sever does not support this http version**

### ***FTP - File Transfer Protocol***
**It is used to transfer files between two computers over a network.**
<br>
***Examples-***
<br>
```
Your Laptop ----Resume.pdf----> Company Server
```
### ***FTP uses TCP***
**File transfer must be reliable. If some packets are lost ,the file is corrupte. Therefore FTP uses TCP**
### ***FTP uses two TCP connection***
- **Control connection - Uses for comand(Username , Passwoprd , Commands)**
<br>
**PORT 21**
<br>

***Examples -***
```
USER saloni
PASS mypassword
GET resume.pdf
PUT project.zip
```
- **Data connection - Uses for actual file transfer**
<br>

***Examples -***
```
resume.pdf
project.zip
image.png
```

### ***FTP Session Example***
***STEP 1***
```
Client ----Port 21----> Server
```
**Control Connection Establish**
<br>
***STEP 2***
```
USER : Saloni
```
***STEP 3***
```
PASS: *******
```
***STEP 4***
```
RETR: notes.pdf
```
**RETR = Retrieve**
<br>

***STEP 5***
<br>
**FTP creates a new data connection**
<br>

***STEP 6***
<br>
**Server send ```notes.pdf``` through data connection**
<br>

***STEP 7***
<br>
**Data connection closes. Control connection remains active**

### ***FTP is Statefull***
**Server remembers information about user from past request**

### ***HTTP vs FTP***
|HTTP|FTP|
|----|---|
|Port 80|Port 21|
|Web pages|File transfer|
|Stateless|Statefull|
|One TCP connection|Two TCP connection|

### ***Important FTP commands***
**USER -** **Tells server your username**
<br>
**PASS -** **Tells server your password**
<br>
**LIST -** **Shows all files in current directory**
<br>
**RETR -** **Retreive a file from server**
<br>
**STOR -** **Store a file on server**

### ***FTP Reply Codes***
**331 -** **User OK password required**
<br>
**425 -** **Can't open data connection**

### ***SMTP - Simple Mail Transfer Protocol***
**It is an application layer for sending emails**
<br>
***Examples -***
```
From: saloni@gmail.com
To: hr@company.com
Subject: Internship Application
```
**SMTP is responsible for  moving this email from your mail server to reciept's mail server. PORT no 25**

### ***How Email Travels ?***
**Alice wants to send email Bob**
<br>

***STEP 1***
<br>
**Alice writes an email and send**
<br>

***STEP 2***
<br>
**Alice's email goes to Alice's mail server .Mail is temporarily stores in a queue**
<br>

***STEP 3***
<br>
**Alice Mail server opens TCP connetion with with Bob's mail server.**

***STEP 4***
<br>
**Alice Mail server sends Email through TCP connection**

***STEP 5***
<br>
**Bob's mail server recievs email and store in Bob's mail box**
```
Alice ---> Alice Mail's server ---SMTP--> Bob's mail server ----> Bob's Mail box ----> Bob read and reply
```

### ***SMTP uses Persistent Connection***
**Persistent connection - connection remains open while multiple mail exchanged.**
<br>
**SMTP uses persistent connection for efficiency**

### ***SMTP is a PUSH Protocol***
**PUSH -** **SMTP actively pushes email to reciever mail server**
<br>
**PULL -** **Reciever request server to give msg. HTTP is a PULL protocol.** 
### ***SMTP vs HTTP***
|SMTP|HTTP|
|----|----|
Push control| Pull control|
|Used for sending mails|Used for web pages|
|PORT 25| PORT 80|
|Persistent connection|Genarly use request - response model|

### ***POP3 and IMAP (Mail access protocols)***
**SMTP - Send Mail**
<br>
**POP3 and IMAP - Recive mail**
<br>

**Mail Sending :**
```
sender device ----> SMTP ----> mail server
```
**Mail Reading :**
```
mail server ----> POP3/IMAP ----> reciever device
```

### ***How POP3(Post Office Protocol Version 3) Works***
***STEP 1***
<br>
**Client connects to mail server through PORT 110**
<br>
***STEP 2***
<br>
**User logs in using Username and Password**
<br>
***STEP 3***
<br>
**Mail is download : ```Mail Server``` ----> ```Client Laptop```**
<br>
***STEP 4***
<br>
**Usually mails are removed from server or marked for deletion**

### ***POP3 Phases***
***Authorization -*** **Login**
<br>
***Examples -***
```
Username: Saloni
Password: ****
```
***Transaction -*** **Operations**
<br>
***Examples -***
```
Download mail
Delete mail
Get statistics
```
***Update -*** **Session ends**
<br>
***Examples -***
```
Messages marked for deletion are removed
```
***POP3 Replies -***
```
+OK - Ok response
-ERR - Bad response
```
***Problem with POP3 -***
<br>
**If  use same email in all laptop,phone and tablet then phone may not see the same state this is inconvinient**

### ***IMAP(Internal Mail Access Protocol)***
**Mail remains on server only copy or required content is fetched**

- ***IMAP remains folder -*** **Server remembers all folder**
- ***IMAP maintains State -*** **Which is read or not read .This property does not work well in POP3**
- ***IMAP provides partial download -*** **If a mail contaion a big video it helps to download only header not full content of mail. This is very usefull for slow network.**

### ***POP3 VS IMAP***
|POP3|IMAP|
|----|----|
|Download mails|Keeps mail on Server|
|Simple|More Advanced|
|Limited SynchroniZation|Full Synchronization|
|Best for single device|Best for multiple devices|
|PORT 110|Commonly PORT 143|
|Usally  removes mails from server|Mails remains on server|

## **DNS (Domain Name System)**
**DNS translates website name to IP address. Uses PORT 53.**
<br>
***Examples -***
<br>

**You type :**
```
www.google.com
```

**Browser asks DNS :**
```
What is the IP address of google.com
```

**DNS Replies :**
```
120.250.xxx.xxx
```

## **Peer to Peer(P2P) Applications and BitTorrent**

**In P2P every computer can Recieve data and send data at the same time**
```
peer <----> peer
```
**But in Client Server**
```
Client -----> Server
```

### ***BitTorrent***
**BitTorrent is a Peer-to-Peer file-sharing protocol in which a file is divided into chunks and users download different chunks from multiple peers simultaneously while also uploading chunks to others. This reduces server load and speeds up distribution**


***Examples -***
<br>
**Download a  movie. Let's divide into 4 chunks**
```
Chunk A
Chunk B
chunk C
Chunk D
```
**Different User download different chunks :**
```
Chunk A -> User 1
Chunk B -> User 2
Chunk C -> User 3
Chunk D -> User 4
```
**Now :**
```
U1 has A
U2 has B
U3 has C
U4 has D
```
**users shares each other :**
```
u1 <---> u2 <---> u3 <---> u4
```
**After sometime :**
```
U1 = A B C D
U2 = A B C D
U3 = A B C D
U4 = A B C D
```
**It is faster bcz in normal client server architecture everyone dowload movie separately so it increases load on server. but in this process the dowloading and uploading occur simultaneously. So it is fast**

#### ***Seeder (has complete file and can share it)***
**After downloading 4 chunks of movie if u keep laptop online u can share chunks to others . so u are becomes Seeder**

#### ***Leecher (Still downloading)***
**If u have chunk A and B . But u need Chun C and D for complete download. so u are leecher**

#### ***Rarest first (Download the rare Chunk first)***
 
```
chunk A - 100 users
chunk B - 59 users
Chunk C - 45 users
Chunk D - 20 Users
```
**then download Chunk D first bcz if these 20 users go offline noone can complete download. So chooose rarest first**

#### ***Tit for Tat (It prefers who sharing)***
**BitTorrent uses the method that which user helps u. U help those users**

## **DHCP(Dynamic Host Configuration Protocol)**

**It solves the question** -
<br>
***"How does your laptop get an IP address when it connects to WiFi?"***
#### ***Problem***
**Suppose you buy a new laptop then you connect to your wifi. But question is that how your laptop know it's IP address, Subnet Mast,Default gateway,DNS server etc.. Means someone provide these things.**

***Ans -*** **That someone is DHCP**

### ***Information provided by DHCP***
- ***IP address -*** **Device identity**
- ***Subnet Mask -*** **Determines network and host portions**
- ***Default Gateway -*** **Usually router. Needed to reach outside networks.**
- ***DNS Server -*** **Usually translate from ```google.com``` to ```8.8.8.8```**


### ***DORA Process***

#### **D = Discover**
**Laptop does not have an IP address. So it Broadcast :**
```
Anyone there?
I need an IP address.
```
#### **O = Offer**
**DHCP server replies :**
```
I can give you:
192.168.1.10
```
#### **R = Request**
**Laptop says :**
```
Yes,
I want 192.168.1.10
```
#### **A = Acknowledgement**
**Server says :**
```
Approved.
Use this IP.
```
#### **Visual Flow**
```
Client
   |
Discover
   ↓
DHCP Server
   |
Offer
   ↓
Client
   |
Request
   ↓
DHCP Server
   |
ACK
   ↓
Client
```

## ***HTTPS(HyperText Transfer Protocol Secure)***
**HTTPS = HTTP + TLS(Transport Layer Security)**
<br>
**Uses PORT 443**
<br>

***Problem in HTTP -***
<br>
**Suppose logging into a website and entering username and password. that basiacly means :**
```
Client ---Username and Password---> Server
```
**Anyone sitting in between can read it. This is called Eavesdropping or Packet Sniffing** 

***Solution -***
<br>
**HTTPS hash the password . evenif someone inside this intercepts it looks meaningless**
```
Real password : 123456
Hash password : x#$%&8bw
```
### **What security does HTTPS provide?**
- ***Confidentiality -*** **No body can read data in between client and srver**
- ***Integrity*** - **No body can modify the data**
- ***Authentication*** - **HTTPS verifies identity using certificates**


### ***What is a certificate ?***
**Certificate is like ID card. Website sends it's certificate and browser verifies it if valid connection build**

### ***What is PKI?***
**PKI is a system that manages digital certificates and public keys to enable secure communication.**
<br>

***Public Key -*** **Every browser uses it for an website**
<br>
***Private key -*** **Only website can decrypt using public key**

### ***HTTP vs HTTPS***
|HTTP|HTTPS|
|----|-----|
|Port 80|Port 443|
|Not encrypted|Encrypted|
|Less secure|More secure|
|Vulnerable to sniffing|Protected|
|Uses HTTP|Uses HTTP+TLS|

***Note -***
```
HTTPS
  ↓
TLS
  ↓
TCP
  ↓
IP
```