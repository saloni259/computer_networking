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


## **UDP Header**
**UDP is connectionless and unreliable**
<br>
**Suppose PC send ```Hello``` to another PC. How does the reciever know :**
```
Which application sent it?
Which application should receive it?
How big is the message?
Was it corrupted?
```
**That's why UDP adds a small header**

### ***UDP Segment Structure***
**UDP header has only 4 fields :**
```
--------------------------------
| Source Port      | Dest Port |
--------------------------------
| Length           | Checksum  |
--------------------------------
| Data                         |
--------------------------------
```
**Only 8 byets header**

- ***Source Port -*** **Used to identify source application**
<br>
- ***Destination Port -*** **Tells reciever Which application should receive data?**
- ***Length -*** **(Header + Data) in bytes**
- ***Checksum -*** **sender send  ```Hello``` and during transmission it corrupted and recieves```Helxo```. so sender calculates a special value and Receiver recalculates it. If both match ```No error detected``` and if not ```Packet corrupted```.** 

### ***UDP Applications***
- ***DNS -*** **Small query and
Need fast response**
- ***DHCP -*** **When device first joins network .It doesn't even have an IP yet and UDP is simpler. So DHCP uses it**
- ***NTP(Network Time Protocol) -***
**Used to synchronize time**


## **Transport Layer**
**The transport layer provides :**
```
Process-to-Process Communication
Getting packet to destination computer
Laptop → Google Server
```
**But Network Layer provides :**
```
Computer-to-Computer Communication
Getting packet to correct application
Google Server → Chrome Process
```

#### ***Problem -***
**In laptop all applications(Chrome, Whatsapp,Zoom etc) are running. So all are using internet simultaneously. When packets arrive to laptop how does OS know whether it belongs to chrome, Whatsapp, Zoom.**
#### ***Solution -***
**Transport Layer provides logical communication between processes running on different hosts.**

***Logical Communication -***
<br>

**Actually -**
```
Your Laptop
     ↓
Router
     ↓
ISP
     ↓
Many Routers
     ↓
Google Server
```
**But it feel like -**
```
Chrome ↔ Google
```
**This illusin is called ```Logical Communication```**

### **Multiplexing and Demultiplexing**
#### ***Multiplexing -***
**Suppose all chrome,whatsapp,zoom wants to send data. Transport layer collects data from all applications combines them and sends them. This is called ```Multiplexing```**
```
Chrome   → Packet A
WhatsApp → Packet B
Spotify  → Packet C
```
#### ***Demultiplexing -***
**After packets arrive at destination it divides and OS decides which packect goes to which application. This separation known as ```Demultiplexing```.**
```
Packet A → Chrome
Packet B → WhatsApp
Packet C → Spotify
```

### **Ports -**
**IP Address identifies Computer similarly Port identifies Application**

***Examples -***
```
Chrome      → Port 5000
WhatsApp    → Port 5001
Spotify     → Port 5002
```

### **Socket -**
**Socket as ```Communication Endpoint```. Applications send/receive data through sockets.**


## **Checksum Calculation**
**Sender calculates a special value**

***Examples -***
```
Data = HELLO
Checksum = XYZ
```
**Sender sends :**
```
HELLO + XYZ
```
**Receiver receives :**
```
HELLO + XYZ
```
**and recalculates checksum**
<br>
- **If ```Calculated Checksum == Received Checksum``` then ```Probably No Error```**
- **If ```Calculated Checksum != Received Checksum``` then ```Packet Corrupted```**


***Note -*** 
- **Checksum does not correct errors it detects error**
- **UDP doesn't guarantee delivery.
But still reciver wants to know ''Did packet get corrupted?'' Checksum provides that information**

## **TCP(Transmission Control Protocol)**

### ***TCP Connection***
**TCP establish a connection before sending a data. This is known as 3 way handshake**

### ***Full Duplex***
**Both sides can send and receive simultaneously.**
```
User1 ----message 1----> User 2
User1 <----message 2---- User 2
```
### ***Point-to-Point***
**TCP connection is**
```
one Sender
onr Reciever
```
**TCP does not support**
```
One Sender
↓
100 Receivers
```
**This is multicasting**

### ***TCP Buffers***
**Sender Buffer and Reciever Buffer**

#### ***Why buffers are needed?***
**Suppose application generates data faster than network can send.**
<br>
***Example -***
<br>
**Suppose 100mb file and network can only send 1mb/sec. Need temporary storage known as ```Buffer```.**

#### ***Send Buffer***
**Application generates data faster than network can send**
```
Application
      ↓
Send Buffer
      ↓
TCP
      ↓
Network
```
#### ***Recieve Buffer***
**Suppose packets arrive quickly and application busy. So Packets wait in recieve Buffer**
```
Network
    ↓
TCP
    ↓
Receive Buffer
    ↓
Application
```

***Note -*** **TCP does not send data immediately. It stores data in send buffer. Then sends data when it appropriate**

### ***MSS (Maximum Segment Size)***
**Maximum amount of application data in one TCP segment.**
<br>
***Example -***
```
MSS = 1460 bytes
Total = 5000 bytes
becomes:
1460
1460
1460
620
```
### ***Why TCP is reliable?***
- **Sequence Numbers**
- **Acknowledgements**
- **Retransmissions**
- **Flow Control**

### ***TCP Segment Structure***
```
------------------------------------------------
| Source Port | Destination Port              |
------------------------------------------------
| Sequence Number                             |
------------------------------------------------
| Acknowledgement Number                      |
------------------------------------------------
| HeaderLen | Flags | Window Size            |
------------------------------------------------
| Checksum | Urgent Pointer                  |
------------------------------------------------
| Data                                         |
------------------------------------------------
```
### **Source Port**
**Which application sent this.**
<br>
***Example -***
```
Chrome → Port 50000
```

### **Destination Port**
**Which application should receive it?**
<br>
***Examples -***
```
HTTPS Server - 443
```

### **Sequence Number**
**Suppose file ```ABCDEFGH``` is split into ```ABC,DEF,GH``` and Network may deliver ```DEF,GH,ABC```. How does reciever rearrange this? So need numbering.**
<br>

***Example -***
<br>
**TCP labels bytes.**
```
A = 0
B = 1
C = 2
D = 3
E = 4
F = 5
G = 6
H = 7
```
**Segments and sequence number**
```
ABC - 0
DEF - 3
GH - 6
```
**Sequence Number = Byte number of the first byte carried by the segment.**

### ***Initial Sequence Number (ISN)***
**Why doesn't TCP always start from 0?**


***Examples -***


**Old connection: ```seq 0```**
<br>
**New Connection: ```seq 0```**
<br>
**Some delayed packet of lod connecton still in network .so in new connction reciever may confuse with old and new packets.**
<br>

***Solution -***
<br>
**TCP choose a random Initial Sequence Number (ISN) instead of 0 .**

### **Acknowledgement Number**
**ACK Number means = Next byte expected by receiver.**
<br>

***Example -***
```
Received: 0-499
ACK: 500
Meaning: Send byte 500 next.
```
### ***Why Sequence + ACK Together?***
***Examples -***
<br>

**Suppose :**
```
Packet 3 lost
```
**Receiver receives :**
```
Packet 1
Packet 2
Packet 4
```
**Receiver sends :**
```
ACK = Start of Packet 3
```
**TCP knows :**
```
Packet 3 missing
```
**and retransmits it. This is the basis of TCP reliability.**

### ***Cumulative Acknowledgement*** 
**TCP acknowledges everything up to the first missing byte.**
<br>

***Example -***
<br>
**Received**
```
0-99
100-199
200-299
```
**Then :**
```
ACK = 300
```
**If :**
```
300-399 Lost
400-499 Received
500-599 Received
```
**Still :**
```
ACK = 300
```
### **Receive Window (Window Size)**
**Purpose : flow control**
<br>
**Receiver tells sender :**
```
I can currently handle
5000 bytes
```
### ***Header Length***
**Purpose :**
<br>
**Tells receiver:**
```
Where header ends
Where actual data starts
```
### ***Flags***
- ***SYN flag -*** **Connection Establishment or 3 way handshake**
- ***ACK flag -*** **Acknowledgement**
- ***FIN flag -*** **Connection Termination (4 way handshake)**
- ***RST flag -*** **Connection Error or immediate reset**
- ***PSH flag -*** **Deliver data immediately**
- ***URG flag -*** **Urgent Data Present**

## **RTT(Round Trip Time) & Timeout**

#### ***The Problem -***
**Suppose sender sends ```Packet A```. What should it do now ?**
```
Option 1 : Wait forever (Bad)
Option 2 : Resend after 1 millisecond (Also bad. Maybe packet is still travelling.)
```

#### ***Defination of Round Trip Time -***
**Time taken for ```Sender--->Reciever``` and ```Reciever--->Sender ACK``` is known as RTT**

### ***EstimatedRTT -***
**Different packet may be have different RTT. So we need to calculate an AvgRTT. so that we can decide how many times we have to wait.**
<br>

***Example -***
```
100 ms
120 ms
90 ms
200 ms
150 ms
```
**So TCP maintains an average ```EstimatedRTT```**
```
EstimatedRTT = (1-alpha)×EstimatedRTT + alpha×SampleRTT
```

### ***DevRTT -***
**How much RTT varies**
<br>

***Examples -***
<br>

**Stable Network**
```
100
101
99
100

Variation : Very small
DevRTT small
```
**Unstable Network**
```
50
250
80
300

Variation : Huge
DevRTT large
```
### ***Timeout Interval***
```
Timeout = EstimatedRTT + 4×DevRTT
```
***Examples -***
<br>
**Suppose :**
```
EstimatedRTT = 100 ms
DevRTT = 20 ms
```
**Then :**
```
Timeout = 100 + 4×20 = 180 ms
```
**TCP waits 180 ms for ACK**
- **If ACK arrives Before 180 ms. It good**
- **If ACK doesn't arrive After 180 ms. TCP assumes Packet Lost and retransmits.**

### ***TCP Flow Control***

#### ***Problem -***
**Suppose sender speed ```100 MB/sec``` but receiver can process only ```10 MB/sec```. So sender keeps transmitting and Receiver cannot keep up. Eventually Receiver Buffer Full and and packets start getting dropped.**
#### ***Solution -*** **Flow Control**
**Preventing the sender from overwhelming the receiver.**

### ***How TCP Solves This?***
**TCP uses ```Receive Window (rwnd)```**.
<br>
**rwnd -** **Receiver tells sender ```I currently have
X bytes free.```**

***Examples -***

**Suppose receiver buffer ```Capacity = 10000 Bytes```. currently used ```4000 Bytes``` and free ```6000 Byets```. Reciever sends ```rwnd = 6000```**
<br>
**It is dynamic in nature.**


### ***Zero Window Problem***

#### ***Situation -***
**Receiver buffer becomes full. Receiver advertises ```rwnd = 0``` meaning ```Stop sending```. 
**Receiver buffer becomes full. Receiver advertises ```rwnd = 0``` meaning ```Stop sending```. Sender stops. Now receiver starts processing data. Buffer becomes free.**
<br>

***Problem -***
```
How does sender know
buffer is free now?
```
***TCP Solution -***
<br>
**TCP periodically sends tiny packets. These are called window probes. Eventually receiver replies: ```rwnd = 5000``` and Sender resumes transmission.**

### ***Difference Between Flow Control and Congestion Control***
***Flow Control -*** **Concern: Receiver Capacity**
<br>
**Congestion Control -** **Concern: Network Capacity**

# TCP Connection Management (3-Way Handshake)

## Why do we need a handshake?

Before sending actual data, both sides need to make sure that:

* The receiver is available.
* Both sides can communicate with each other.
* Initial sequence numbers are exchanged.

---

## 3-Way Handshake Steps

```text
SYN
SYN-ACK
ACK
```

---

### Step 1: SYN

Client sends:

```text
SYN
Seq = 100
```

Meaning:

> I want to establish a connection and my starting sequence number is 100.

`SYN` stands for:

```text
Synchronize Sequence Numbers
```

---

### Step 2: SYN + ACK

Server replies:

```text
SYN
ACK
Seq = 500
ACK = 101
```

Meaning:

* Server received the SYN.
* Server accepts the connection.
* Server's sequence number starts from 500.
* Server expects byte 101 next.

Why ACK = 101?

```text
SYN consumes one sequence number.

100 + 1 = 101
```

---

### Step 3: ACK

Client sends:

```text
ACK
Seq = 101
ACK = 501
```

Meaning:

* Client received the server's SYN.
* Client expects byte 501 next.

---

## Diagram

```text
Client                    Server

SYN Seq=100
------------------------->

               SYN+ACK
      Seq=500 ACK=101
<-------------------------

ACK
Seq=101 ACK=501
------------------------->

Connection Established
```

---

## Example

Phone call example:

```text
You: Hello?
Friend: Hello.
You: Can you hear me?
Friend: Yes.
```

After confirmation, the conversation starts.

---

## Why not 2-Way Handshake?

If only:

```text
SYN
SYN+ACK
```

were exchanged, the server would never know whether the client actually received the `SYN+ACK`.

The final ACK confirms this.

---

## Why not 4-Way Handshake?

TCP combines:

```text
SYN + ACK
```

into a single packet, reducing the number of steps from 4 to 3.

---

## Quick Revision

```text
SYN     -> Start connection
SYN+ACK -> Accept connection
ACK     -> Confirmation
```

---

# TCP Connection Termination (4-Way Handshake)

After communication finishes, TCP closes the connection using four steps.

---

### Step 1: FIN

Client sends:

```text
FIN
Seq = 100
```

Meaning:

> I have finished sending data.

---

### Step 2: ACK

Server replies:

```text
ACK = 101
```

Meaning:

> I received your FIN.

The server may still have some data left to send.

---

### Step 3: FIN

After sending its remaining data, the server sends:

```text
FIN
Seq = 500
```

Meaning:

> I have also finished sending data.

---

### Step 4: ACK

Client replies:

```text
ACK = 501
```

Meaning:

> I received your FIN.

Connection closes.

---

## Diagram

```text
Client                          Server

FIN Seq=100
------------------------------->

                     ACK=101
<-------------------------------

                     FIN Seq=500
<-------------------------------

ACK=501
------------------------------->

Connection Closed
```

---

## Why does TCP need 4 steps?

During connection setup:

```text
SYN + ACK
```

can be combined.

During termination, one side may still have data left to send, so:

```text
ACK
```

and

```text
FIN
```

cannot always be sent together.

---

## FIN vs ACK

### FIN

```text
I won't send any more data.
```

### ACK

```text
I received your message.
```

---

## TIME_WAIT State

After sending the final ACK, the client waits for some time before completely closing the connection.

Reason:

If the last ACK gets lost, the server may send FIN again and the client should still be able to respond.

---

## Quick Revision

```text
FIN -> I am done sending.
ACK -> I received your message.
```

---

# TCP Congestion Control

Congestion control prevents the network from becoming overloaded.

---

## Example

Suppose a road can handle:

```text
1000 cars/minute
```

but suddenly:

```text
5000 cars/minute
```

try to use it.

Result:

```text
Traffic Jam
```

The same thing happens in computer networks.

---

## Congestion Window (cwnd)

TCP uses:

```text
cwnd
```

to decide how much data can be sent into the network at one time.

---

## Example

Suppose:

```text
cwnd = 3 packets
```

Sender sends:

```text
Packet 1
Packet 2
Packet 3
```

and waits for ACKs before sending more packets.

---

## Formula

```text
Data in Transit <= min(rwnd, cwnd)
```

where:

```text
rwnd = Receiver Window
cwnd = Congestion Window
```

---

## Slow Start

Initially:

```text
cwnd = 1
```

After every RTT:

```text
1 -> 2 -> 4 -> 8 -> 16
```

The congestion window doubles every round trip time.

---

## Why is it called Slow Start?

Because TCP starts with only one packet instead of flooding the network immediately.

---

## Congestion Detection

If TCP detects:

```text
Timeout
or
Duplicate ACKs
```

it assumes congestion in the network and reduces `cwnd`.

---

## Congestion Avoidance

Instead of increasing exponentially:

```text
1 -> 2 -> 4 -> 8 -> 16
```

TCP starts increasing slowly:

```text
16 -> 17 -> 18 -> 19
```

---

## Fast Retransmit

Suppose sender receives:

```text
ACK = 500
ACK = 500
ACK = 500
```

three times.

TCP immediately retransmits the missing packet without waiting for timeout.

---

## Fast Recovery

After Fast Retransmit, TCP reduces the congestion window partially instead of resetting it to 1.

---

## Flow Control vs Congestion Control

| Flow Control      | Congestion Control |
| ----------------- | ------------------ |
| Protects receiver | Protects network   |
| Uses rwnd         | Uses cwnd          |
| Receiver issue    | Network issue      |

---

## Quick Revision

```text
rwnd -> Receiver limitation
cwnd -> Network limitation

Flow Control -> Protect receiver
Congestion Control -> Protect network
```


