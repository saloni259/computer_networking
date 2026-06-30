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

# Network Layer - Forwarding vs Routing

The main job of the Network Layer is to move packets from the source device to the destination device.

Example:

```text
My Laptop
   ↓
Router
   ↓
Internet
   ↓
Google Server
```

To do this, the network layer performs two important functions:

* Routing
* Forwarding

---

# Routing

Routing means deciding the complete path that a packet should follow from source to destination.

Example:

```text
Laptop
 ↓
Router A
 ↓
Router B
 ↓
Router C
 ↓
Google Server
```

Routing decides whether the packet should go through:

```text
A → B → C
```

or

```text
A → D → E → C
```

It is basically route planning.

---

## Real Life Example

Suppose you want to travel from Kolkata to Delhi.

You have multiple routes:

```text
Kolkata → Patna → Delhi
```

or

```text
Kolkata → Lucknow → Delhi
```

Choosing the route is called **Routing**.

---

# Forwarding

Forwarding means moving a packet from the incoming interface of a router to the correct outgoing interface.

Example:

```text
Laptop
 ↓
Router A
 ↓
Router B
 ↓
Router C
 ↓
Google Server
```

When the packet reaches Router B, Router B only needs to decide:

```text
Which port should I send this packet to next?
```

For example:

```text
Incoming Port = 1
Outgoing Port = 3
```

This process is called **Forwarding**.

---

## Real Life Example

Suppose you are already in Patna and now need to decide which road to take to reach Delhi.

Choosing the next road from the current location is called **Forwarding**.

---

# Easy Way to Remember

```text
Routing   -> Decides the complete path.
Forwarding -> Sends packet to the next hop.
```

---

# Another Example

Imagine a courier service.

Routing department decides:

```text
Kolkata
 ↓
Patna Hub
 ↓
Delhi Hub
 ↓
Customer
```

This is routing.

At Patna Hub, deciding which truck should carry the parcel next is forwarding.

---

# Routing vs Forwarding

| Routing                         | Forwarding               |
| ------------------------------- | ------------------------ |
| Decides complete path           | Moves packet to next hop |
| Global decision                 | Local decision           |
| Happens in all routers together | Happens inside a router  |
| Uses routing table              | Uses forwarding table    |
| Part of Control Plane           | Part of Data Plane       |

---

# Data Plane vs Control Plane

## Data Plane

Responsible for actually moving packets.

Example:

```text
Packet arrives at Router B
↓
Router sends packet to Router C
```

This is forwarding.

---

## Control Plane

Responsible for building routes and routing tables.

Example:

```text
Best path to Google:
Router A → Router B → Router C
```

This is routing.

---

# Routing Protocols

Routers exchange information using routing protocols such as:

* RIP
* OSPF
* BGP

These protocols help routers decide the best path.

---

# Quick Revision

```text
Routing   -> Path Selection
Forwarding -> Packet Movement

Routing   -> Control Plane
Forwarding -> Data Plane

Routing   -> Global Decision
Forwarding -> Local Decision
```
# IPv4 (Internet Protocol Version 4)

An IP address is a unique logical address given to every device connected to a network.

Example:

```text
192.168.1.10
```

You can think of it as the home address of a computer.

Without an IP address, devices on the internet would not know where to send data.

---

# Why do we need IP addresses?

Suppose your laptop wants to send data to Google.

```text
My Laptop
    ↓
Router
    ↓
Internet
    ↓
Google Server
```

The packet needs an address to know where it should go.

That address is called the IP address.

---

# IPv4 Address Format

IPv4 uses:

```text
32 bits
```

These 32 bits are divided into:

```text
4 parts (octets)
```

Example:

```text
192.168.1.10
```

Each part contains:

```text
8 bits
```

So:

```text
8 + 8 + 8 + 8 = 32 bits
```

---

# Binary Representation

Example:

```text
192.168.1.10
```

in binary becomes:

```text
11000000.10101000.00000001.00001010
```

---

# Range of Each Octet

Since each octet contains 8 bits:

Minimum value:

```text
00000000 = 0
```

Maximum value:

```text
11111111 = 255
```

Therefore every part of an IPv4 address lies between:

```text
0 to 255
```

---

# Network ID and Host ID

An IPv4 address consists of two parts:

* Network ID
* Host ID

Example:

```text
192.168.1.25
```

can be divided as:

```text
Network ID = 192.168.1
Host ID    = 25
```

---

## Real Life Example

Think of an apartment building.

```text
Apartment Building Number -> Network ID
Flat Number               -> Host ID
```

The building identifies the network and the flat identifies the device inside that network.

---

# Why do we separate Network ID and Host ID?

When a packet arrives:

1. Router first finds the destination network.
2. Then it finds the destination device inside that network.

---

# IPv4 Classes

## Class A

Range:

```text
1.x.x.x to 126.x.x.x
```

Default subnet mask:

```text
255.0.0.0
```

Used for very large organizations.

---

## Class B

Range:

```text
128.x.x.x to 191.x.x.x
```

Default subnet mask:

```text
255.255.0.0
```

Used for medium sized organizations.

---

## Class C

Range:

```text
192.x.x.x to 223.x.x.x
```

Default subnet mask:

```text
255.255.255.0
```

Used for small organizations.

---

## Class D

Range:

```text
224.x.x.x to 239.x.x.x
```

Used for:

```text
Multicasting
```

---

## Class E

Range:

```text
240.x.x.x to 255.x.x.x
```

Used for:

```text
Research and Experimental purposes
```

---

# Easy Memory Trick

```text
A -> Large organizations
B -> Medium organizations
C -> Small organizations
D -> Multicast
E -> Experimental
```

---

# Public IP vs Private IP

## Public IP

* Visible on the internet.
* Assigned by ISP.
* Globally unique.

Example:

```text
49.204.x.x
```

---

## Private IP

Used inside homes and offices.

Private IP ranges:

```text
10.0.0.0      - 10.255.255.255
172.16.0.0    - 172.31.255.255
192.168.0.0   - 192.168.255.255
```

These addresses cannot be accessed directly from the internet.

---

## Example

Your laptop may have:

```text
192.168.1.5
```

inside your home network.

But your router may have:

```text
49.204.x.x
```

as the public IP assigned by the ISP.

---

# Why was IPv6 introduced?

IPv4 provides:

```text
2^32 ≈ 4.3 Billion addresses
```

This seemed enough in the 1980s.

Today we have:

* Phones
* Laptops
* Smart TVs
* Smart Watches
* IoT Devices
* Cameras

As a result, IPv4 addresses started running out.

To solve this problem:

```text
IPv6
```

was introduced.

---

# Quick Revision

```text
IPv4 -> 32 bits
4 Octets
Each octet ranges from 0 to 255

IP Address = Network ID + Host ID

Public IP -> Internet Accessible
Private IP -> Used inside LAN

IPv6 was introduced because IPv4 addresses are limited.
```
# IPv6 (Internet Protocol Version 6)

IPv6 was introduced because IPv4 addresses started running out.

IPv4 provides:

```text
2^32 ≈ 4.3 Billion addresses
```

Earlier this looked huge, but today we have:

* Phones
* Laptops
* Tablets
* Smart TVs
* Smart Watches
* IoT Devices
* Cameras

So a larger address space was needed.

---

# What is IPv6?

IPv6 is the next generation of Internet Protocol.

It uses:

```text
128 bits
```

instead of:

```text
32 bits
```

used in IPv4.

---

# Number of Addresses

IPv4:

```text
2^32 ≈ 4.3 Billion
```

IPv6:

```text
2^128
```

which is approximately:

```text
340 undecillion addresses
```

This number is so large that running out of addresses is practically impossible.

---

# IPv6 Address Format

IPv4 Example:

```text
192.168.1.10
```

IPv6 Example:

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Notice:

* IPv4 uses dots (`.`)
* IPv6 uses colons (`:`)

---

# Structure of IPv6 Address

IPv6 contains:

```text
8 groups
```

Each group contains:

```text
4 hexadecimal digits
```

Example:

```text
2001
0db8
85a3
0000
0000
8a2e
0370
7334
```

---

# Why Hexadecimal?

If decimal numbers were used, IPv6 addresses would become extremely long.

Hexadecimal notation makes them shorter and easier to read.

---

# IPv6 Address Compression

Leading zeros can be removed.

Example:

```text
2001:0db8:0000:0000:0000:0000:0000:0001
```

can be written as:

```text
2001:db8::1
```

The `::` represents multiple groups of zeros.

---

# Advantages of IPv6

## Huge Address Space

The biggest advantage of IPv6 is the massive number of available addresses.

---

## Better Security

IPv6 was designed with support for:

```text
IPSec
```

which provides security and encryption features.

---

## No Need for NAT in Most Cases

With IPv4:

```text
Many Private IPs
↓
One Public IP
```

using NAT.

With IPv6, every device can potentially have its own public IP address.

---

## Simpler Routing

IPv6 routing tables are more efficient and scalable.

---

# IPv4 vs IPv6

| IPv4                        | IPv6                            |
| --------------------------- | ------------------------------- |
| 32-bit                      | 128-bit                         |
| Uses dots (.)               | Uses colons (:)                 |
| About 4.3 Billion addresses | 2^128 addresses                 |
| Address exhaustion problem  | Practically unlimited addresses |
| Example: 192.168.1.1        | Example: 2001:db8::1            |

---

# Easy Memory Trick

```text
IPv4 -> 32 bits -> Dots (.)
IPv6 -> 128 bits -> Colons (:)
```

---

# Quick Revision

```text
IPv4 -> 32-bit
IPv6 -> 128-bit

IPv4 uses decimal numbers.
IPv6 uses hexadecimal numbers.

IPv6 was introduced because IPv4 addresses are limited.

IPv6 addresses use colons instead of dots.
```
# ICMP (Internet Control Message Protocol)

ICMP is used for sending error messages and control information in a network.

IP itself cannot report errors, so it uses ICMP for this purpose.

---

# Why do we need ICMP?

Suppose your computer sends a packet to a server but:

* The server does not exist.
* The destination network is unreachable.
* The packet gets stuck in a loop.

Your computer needs to know what went wrong.

ICMP provides this information.

---

# Example

Suppose your laptop sends a packet to:

```text
google.com
```

but the destination cannot be reached.

Instead of silently dropping the packet, the network sends back an error message using ICMP.

---

# Common ICMP Messages

## Destination Unreachable

This message is sent when:

* The destination host is down.
* The destination network does not exist.
* The destination port is closed.

Example:

```text
Destination Host Unreachable
```

---

## Time Exceeded

Packets use a field called:

```text
TTL (Time To Live)
```

Every router decreases the TTL value by 1.

Example:

```text
Initial TTL = 5

Router 1 -> TTL = 4
Router 2 -> TTL = 3
Router 3 -> TTL = 2
Router 4 -> TTL = 1
Router 5 -> TTL = 0
```

When TTL becomes 0:

* The router drops the packet.
* An ICMP Time Exceeded message is sent back.

This prevents packets from travelling forever in routing loops.

---

## Parameter Problem

If the IP header contains invalid or corrupted information, the router sends:

```text
ICMP Parameter Problem
```

---

## Source Quench

This message was historically used to tell the sender:

```text
Slow down, the network is congested.
```

This message is now obsolete and is no longer used in modern networks.

---

# Ping and ICMP

The `ping` command uses ICMP.

When you run:

```bash
ping google.com
```

your computer sends:

```text
ICMP Echo Request
```

Google replies with:

```text
ICMP Echo Reply
```

If the reply arrives successfully, the host is reachable.

---

## Example

```text
Laptop
   |
Echo Request
   ↓
Google Server
   |
Echo Reply
   ↑
Laptop
```

---

# Traceroute and ICMP

Traceroute is used to find all routers between source and destination.

Example:

```text
Laptop
 ↓
Router 1
 ↓
Router 2
 ↓
Router 3
 ↓
Google Server
```

Traceroute works using:

* TTL values
* ICMP Time Exceeded messages

---

# Important Points

```text
ICMP is used for error reporting.
ICMP works with IP at the Network Layer.
ICMP does not carry application data.
Ping uses ICMP.
Traceroute uses ICMP.
```

---

# Quick Revision

```text
ICMP -> Error Reporting Protocol

Ping -> Echo Request + Echo Reply

TTL reaches 0 -> Time Exceeded

Destination not reachable -> Destination Unreachable

Traceroute uses ICMP Time Exceeded messages
```
# OSPF (Open Shortest Path First)

OSPF is a routing protocol used by routers to find the best path between source and destination.

It is a **Link State Routing Protocol**.

---

# Why do we need OSPF?

Suppose Router A wants to send data to Router D.

There are two possible paths:

```text
Path 1:
A -> B -> D
Cost = 20

Path 2:
A -> C -> D
Cost = 10
```

OSPF chooses:

```text
A -> C -> D
```

because it has lower cost.

---

# Link State Routing

In OSPF, every router shares information about:

* Its neighbors
* Link costs
* Network status

As a result, every router knows the complete network topology.

---

# Example

```text
      B
    /   \
   5     2
  /       \
 A         D
  \       /
   1     4
    \   /
      C
```

Possible paths from A to D:

```text
A -> B -> D = 5 + 2 = 7

A -> C -> D = 1 + 4 = 5
```

OSPF chooses:

```text
A -> C -> D
```

because:

```text
5 < 7
```

---

# Algorithm Used

OSPF uses:

```text
Dijkstra's Shortest Path Algorithm
```

also called:

```text
Shortest Path First (SPF) Algorithm
```

---

# Cost in OSPF

OSPF selects routes based on:

```text
Cost
```

and not on:

```text
Hop Count
```

---

## Example

Route 1:

```text
A -> B -> D
Hop Count = 2
Cost = 100
```

Route 2:

```text
A -> C -> E -> D
Hop Count = 3
Cost = 20
```

OSPF chooses:

```text
A -> C -> E -> D
```

because the cost is lower.

---

# DR and BDR

OSPF uses:

```text
DR  -> Designated Router
BDR -> Backup Designated Router
```

---

# Why are DR and BDR needed?

Suppose there are:

```text
10 routers
```

If every router communicates with every other router:

```text
10 × 9 = 90 communications
```

This creates a lot of overhead.

Instead:

* All routers communicate with the DR.
* DR distributes the information.
* If DR fails, BDR takes over.

---

# DR Election

Rules for DR selection:

1. Highest Router Priority wins.
2. If priorities are equal:

   * Highest Loopback IP wins.
   * If loopback is not present, highest active interface IP wins.

---

# OSPF Characteristics

```text
Type      : Link State Routing Protocol
Algorithm : Dijkstra Algorithm
Metric    : Cost
Convergence : Fast
Used For  : Large Networks
```

---

# OSPF vs RIP

| OSPF                        | RIP                         |
| --------------------------- | --------------------------- |
| Link State Protocol         | Distance Vector Protocol    |
| Uses Cost                   | Uses Hop Count              |
| Uses Dijkstra Algorithm     | Uses Bellman Ford Algorithm |
| Fast Convergence            | Slow Convergence            |
| Suitable for Large Networks | Suitable for Small Networks |

---

# Quick Revision

```text
OSPF -> Open Shortest Path First

Type -> Link State Routing Protocol

Algorithm -> Dijkstra Algorithm

Metric -> Cost

Uses DR and BDR

Suitable for Large Networks
```
# RIP (Routing Information Protocol)

RIP is a routing protocol used by routers to find the path from source to destination.

It is a **Distance Vector Routing Protocol**.

---

# How does RIP choose a path?

RIP chooses the path with the smallest:

```text
Hop Count
```

A hop means passing through one router.

---

# Example

Suppose Router A wants to send data to Router D.

There are two possible paths:

```text
Path 1:
A -> B -> D
Hop Count = 2
```

```text
Path 2:
A -> C -> E -> D
Hop Count = 3
```

RIP chooses:

```text
A -> B -> D
```

because:

```text
2 < 3
```

---

# What is Hop Count?

A hop is simply one router crossed by the packet.

Example:

```text
Laptop
 ↓
Router A
 ↓
Router B
 ↓
Google Server
```

Hop Count:

```text
2
```

because the packet passed through two routers.

---

# Algorithm Used

RIP uses:

```text
Bellman-Ford Algorithm
```

to calculate routes.

---

# Maximum Hop Count

RIP supports a maximum hop count of:

```text
15
```

If hop count becomes:

```text
16
```

the destination is considered unreachable.

---

# Example

```text
Hop Count = 10
```

Destination is reachable.

```text
Hop Count = 16
```

Destination is unreachable.

---

# How RIP Works

Routers periodically share their routing tables with neighboring routers.

Example:

```text
Router A:
I can reach Google in 3 hops.

Router B:
I can reach Google in 2 hops.
```

Router A updates its table accordingly.

---

# Problem with RIP

Suppose there are two routes:

Route 1:

```text
Hop Count = 2
Very Slow Network
```

Route 2:

```text
Hop Count = 4
Very Fast Network
```

RIP still chooses:

```text
Hop Count = 2
```

because RIP only considers hop count and ignores bandwidth or delay.

---

# RIP Characteristics

```text
Type        : Distance Vector Routing Protocol
Algorithm   : Bellman-Ford Algorithm
Metric      : Hop Count
Max Hops    : 15
Convergence : Slow
Used For    : Small Networks
```

---

# RIP vs OSPF

| RIP                         | OSPF                        |
| --------------------------- | --------------------------- |
| Distance Vector Protocol    | Link State Protocol         |
| Uses Hop Count              | Uses Cost                   |
| Uses Bellman-Ford Algorithm | Uses Dijkstra Algorithm     |
| Slow Convergence            | Fast Convergence            |
| Suitable for Small Networks | Suitable for Large Networks |

---

# Easy Way to Remember

```text
RIP  -> Router count matters
OSPF -> Cost matters
```

---

# Quick Revision

```text
RIP -> Routing Information Protocol

Type -> Distance Vector Routing Protocol

Algorithm -> Bellman-Ford Algorithm

Metric -> Hop Count

Maximum Hop Count -> 15

Suitable for Small Networks
```
# ARP (Address Resolution Protocol)

ARP is used to find the MAC address of a device when we already know its IP address.

In simple words:

```text
IP Address  --->  MAC Address
```

---

# Why do we need ARP?

Suppose your laptop wants to send data to another device in the same network.

Your laptop knows:

```text
Destination IP Address = 192.168.1.20
```

But actual communication inside a LAN happens using:

```text
MAC Address
```

So the question becomes:

```text
How do we find the MAC address from the IP address?
```

The answer is:

```text
ARP
```

---

# Example

Suppose we have two devices:

```text
Laptop A
IP  = 192.168.1.10
MAC = AA-AA-AA
```

```text
Laptop B
IP  = 192.168.1.20
MAC = BB-BB-BB
```

Laptop A wants to send data to Laptop B.

Laptop A knows:

```text
192.168.1.20
```

but it does not know:

```text
BB-BB-BB
```

So ARP is used.

---

# Step 1: ARP Request

Laptop A sends a message to everyone in the network:

```text
Who has IP 192.168.1.20 ?
Tell 192.168.1.10
```

This is called:

```text
ARP Request
```

ARP Request is a:

```text
Broadcast Message
```

because it is sent to all devices in the LAN.

---

# Step 2: ARP Reply

Laptop B checks the request and finds:

```text
192.168.1.20 is my IP address.
```

So it replies:

```text
192.168.1.20 is at BB-BB-BB
```

This is called:

```text
ARP Reply
```

ARP Reply is a:

```text
Unicast Message
```

because it is sent only to Laptop A.

---

# Step 3: Store in ARP Cache

Laptop A stores:

```text
192.168.1.20 -> BB-BB-BB
```

inside its:

```text
ARP Cache
```

so it doesn't need to ask again next time.

---

# Diagram

```text
Laptop A                          Laptop B
192.168.1.10                      192.168.1.20

ARP Request:
Who has 192.168.1.20 ?
-------------------------------------->

ARP Reply:
192.168.1.20 is BB-BB-BB
<--------------------------------------

Communication Starts
```

---

# ARP Cache

ARP Cache stores:

```text
IP Address -> MAC Address
```

Example:

| IP Address   | MAC Address |
| ------------ | ----------- |
| 192.168.1.1  | AA-AA-AA    |
| 192.168.1.20 | BB-BB-BB    |
| 192.168.1.30 | CC-CC-CC    |

---

# Why use ARP Cache?

Without cache:

```text
Every packet
↓
ARP Request
↓
ARP Reply
```

This would waste network bandwidth.

---

# Broadcast vs Unicast

```text
ARP Request -> Broadcast
ARP Reply   -> Unicast
```

This is a very common interview question.

---

# IP Address vs MAC Address

| IP Address       | MAC Address             |
| ---------------- | ----------------------- |
| Logical Address  | Physical Address        |
| Can change       | Usually fixed           |
| Used for Routing | Used for Local Delivery |
| Network Layer    | Data Link Layer         |

---

# Important Point

If your computer wants to send data to Google:

```text
www.google.com
```

your computer does NOT find Google's MAC address.

Instead, it finds the MAC address of:

```text
Default Gateway (Router)
```

because Google is outside your local network.

This is a very common interview question.

---

# Easy Way to Remember

```text
DNS -> Domain Name to IP Address

ARP -> IP Address to MAC Address

NAT -> Private IP to Public IP
```

---

# Quick Revision

```text
ARP -> Address Resolution Protocol

ARP converts:
IP Address -> MAC Address

ARP Request -> Broadcast

ARP Reply -> Unicast

ARP Cache stores:
IP Address -> MAC Address mapping
```
# NAT (Network Address Translation)

NAT is used to convert private IP addresses into public IP addresses and vice versa.

In simple words:

```text
Private IP  --->  Public IP
```

---

# Why do we need NAT?

Suppose your home has:

* Laptop
* Phone
* Smart TV
* Tablet

Their IP addresses are:

```text
Laptop   -> 192.168.1.2
Phone    -> 192.168.1.3
TV       -> 192.168.1.4
Tablet   -> 192.168.1.5
```

But your ISP provides only one public IP:

```text
49.204.100.50
```

The question is:

```text
How can all devices use the internet using only one public IP?
```

The answer is:

```text
NAT
```

---

# Example

Suppose your laptop wants to open Google.

Before NAT:

```text
Source IP      = 192.168.1.2
Destination IP = Google's IP
```

Problem:

```text
192.168.1.2
```

is a private IP and private IPs cannot travel on the internet.

---

# NAT Translation

The router changes:

```text
192.168.1.2
```

to

```text
49.204.100.50
```

Now the packet becomes:

```text
Source IP      = 49.204.100.50
Destination IP = Google's IP
```

Google receives the packet successfully.

---

# Reply from Google

Google sends the response back to:

```text
49.204.100.50
```

The router checks its NAT table and finds:

```text
49.204.100.50:6001
↓
192.168.1.2:5001
```

The router then forwards the packet to the laptop.

---

# NAT Table Example

| Private IP  | Private Port | Public IP     | Public Port |
| ----------- | ------------ | ------------- | ----------- |
| 192.168.1.2 | 5001         | 49.204.100.50 | 6001        |
| 192.168.1.3 | 5002         | 49.204.100.50 | 6002        |
| 192.168.1.4 | 5003         | 49.204.100.50 | 6003        |

This allows multiple devices to share a single public IP address.

---

# Why are Port Numbers Needed?

Suppose both laptop and phone open Google at the same time.

Both use:

```text
49.204.100.50
```

as their public IP.

The router uses port numbers to identify which packet belongs to which device.

Example:

```text
Laptop -> Public Port 6001
Phone  -> Public Port 6002
```

---

# Types of NAT

## Static NAT

```text
One Private IP
↓
One Public IP
```

Fixed mapping between private and public IP.

---

## Dynamic NAT

```text
Many Private IPs
↓
Pool of Public IPs
```

Public IP is assigned dynamically from a pool.

---

## PAT (Port Address Translation)

```text
Many Private IPs
↓
One Public IP
```

using different port numbers.

This is the type of NAT commonly used in home routers.

---

# Why is NAT Important?

### Saves IPv4 addresses

Without NAT:

```text
Every device
↓
Needs its own public IP
```

IPv4 addresses would have run out much earlier.

---

### Improves Security

Devices using private IP addresses are not directly accessible from the internet.

---

### Reduces Cost

The ISP only needs to provide one public IP instead of many.

---

# Private IP Address Ranges

```text
10.0.0.0      - 10.255.255.255
172.16.0.0    - 172.31.255.255
192.168.0.0   - 192.168.255.255
```

These addresses are reserved for private networks.

---

# Example from Real Life

Think of an apartment building.

Inside the building:

```text
Flat 101
Flat 102
Flat 103
Flat 104
```

Outside the world only sees:

```text
ABC Apartment,
Kolkata
```

Similarly:

```text
Many Private IPs
↓
One Public IP
```

---

# Easy Way to Remember

```text
DNS -> Domain Name to IP Address

ARP -> IP Address to MAC Address

NAT -> Private IP to Public IP
```

---

# Quick Revision

```text
NAT -> Network Address Translation

Private IP -> Public IP

Performed by -> Router

Home routers mostly use:
PAT (Port Address Translation)

Purpose:
- Save IPv4 addresses
- Improve security
- Allow multiple devices to share one public IP
```
# Hub vs Switch vs Router

These three devices are used to connect devices in a network, but they work in different ways.

---

# Hub

A Hub is a simple networking device that sends incoming data to every connected device.

Example:

```text
Laptop A
   |
  Hub
 / | \
B  C  D
```

If A sends data to C, the hub forwards the data to:

```text
B
C
D
```

Every device receives the packet even though only C needs it.

---

## Problems with Hub

* Wastes bandwidth.
* Less secure because everyone receives the packet.
* More collisions occur.

---

## OSI Layer

```text
Physical Layer (Layer 1)
```

Hub only works with electrical signals.

It does not understand:

* MAC Address
* IP Address
* Port Number

---

# Switch

A Switch is an intelligent device that sends data only to the destination device.

Example:

```text
Laptop A
   |
 Switch
 / | \
B  C  D
```

If A sends data to C, the switch sends data only to:

```text
C
```

---

## How does Switch know where to send the data?

A switch maintains a:

```text
MAC Address Table
```

Example:

| MAC Address | Port |
| ----------- | ---- |
| AA-AA       | 1    |
| BB-BB       | 2    |
| CC-CC       | 3    |

If destination MAC address is:

```text
CC-CC
```

the switch forwards the packet to:

```text
Port 3
```

---

## Advantages of Switch

* Better speed.
* Better security.
* Fewer collisions.

---

## OSI Layer

```text
Data Link Layer (Layer 2)
```

Switch works using:

```text
MAC Address
```

---

# Router

A Router is used to connect different networks.

Example:

```text
Home Network
     |
   Router
     |
Internet
     |
Google Server
```

The router decides the best path for packets to reach another network.

---

## How does Router work?

Router uses:

```text
IP Address
```

to forward packets.

Example:

```text
Destination IP:
142.250.xxx.xxx
```

Router checks its routing table and forwards the packet.

---

## OSI Layer

```text
Network Layer (Layer 3)
```

Router works using:

```text
IP Address
```

---

# Collision Domain

A collision occurs when two devices send data at the same time.

## Hub

```text
Entire Hub = One Collision Domain
```

## Switch

```text
Each Port = Separate Collision Domain
```

## Router

```text
Each Interface = Separate Collision Domain
```

---

# Broadcast Domain

Broadcast means sending a message to everyone.

## Hub

```text
One Broadcast Domain
```

## Switch

```text
One Broadcast Domain
```

## Router

```text
Each Interface = Separate Broadcast Domain
```

Routers break broadcast domains.

---

# Comparison Table

| Feature            | Hub      | Switch          | Router            |
| ------------------ | -------- | --------------- | ----------------- |
| OSI Layer          | Layer 1  | Layer 2         | Layer 3           |
| Uses               | Signals  | MAC Address     | IP Address        |
| Sends Data To      | Everyone | Specific Device | Specific Network  |
| Collision Domain   | One      | One per Port    | One per Interface |
| Broadcast Domain   | One      | One             | Multiple          |
| Intelligent Device | No       | Yes             | Yes               |

---

# Easy Way to Remember

```text
Hub    -> Send to Everyone
Switch -> Send to Device
Router -> Send to Network
```

---

# Quick Revision

```text
Hub
- Layer 1
- Uses Signals
- Sends data to everyone

Switch
- Layer 2
- Uses MAC Address
- Sends data to specific device

Router
- Layer 3
- Uses IP Address
- Connects different networks
```

# MAC Address vs IP Address

Both MAC Address and IP Address are used for communication in a network, but they serve different purposes.

---

# IP Address

IP Address is a logical address used to identify a device across different networks.

Example:

```text
192.168.1.10
```

or

```text
2405:201:abcd::1
```

Routers use IP addresses to send packets from one network to another.

---

# MAC Address

MAC Address is a physical address assigned to the Network Interface Card (NIC) of a device.

Example:

```text
AA:BB:CC:DD:EE:FF
```

Switches use MAC addresses to deliver frames inside a local network.

---

# Example

Suppose:

```text
Laptop IP  = 192.168.1.10
Laptop MAC = AA-AA-AA

Phone IP   = 192.168.1.20
Phone MAC  = BB-BB-BB
```

When the laptop sends data to the phone:

Router uses:

```text
192.168.1.20
```

to identify the destination network.

Switch uses:

```text
BB-BB-BB
```

to identify the destination device.

---

# Why do we need both?

Think of sending a letter.

```text
City + House Address -> IP Address
Person Name Plate    -> MAC Address
```

The post office uses the address to reach the city.

After reaching the house, the postman uses the name plate to identify the correct person.

Similarly:

```text
IP Address  -> Which Network?
MAC Address -> Which Device?
```

---

# Can IP Address Change?

Yes.

Example:

```text
Today:
192.168.1.10

Tomorrow:
192.168.1.15
```

The IP address may change when reconnecting to WiFi or changing networks.

---

# Can MAC Address Change?

Normally:

```text
No
```

because it is assigned by the manufacturer to the network card.

Example:

```text
AA:BB:CC:DD:EE:FF
```

usually remains the same.

---

# Who Uses Them?

## Switch

Uses:

```text
MAC Address
```

---

## Router

Uses:

```text
IP Address
```

---

# OSI Layer

## MAC Address

```text
Data Link Layer (Layer 2)
```

---

## IP Address

```text
Network Layer (Layer 3)
```

---

# Complete Communication Example

Suppose your laptop opens Google.

Step 1:

```text
google.com
↓
142.250.xxx.xxx
```

DNS converts domain name into IP address.

---

Step 2:

Router uses:

```text
142.250.xxx.xxx
```

to forward packets towards Google.

---

Step 3:

Inside your local network, the router uses:

```text
Laptop MAC Address
```

to deliver packets to your laptop.

---

# Comparison Table

| Feature | MAC Address       | IP Address       |
| ------- | ----------------- | ---------------- |
| Type    | Physical Address  | Logical Address  |
| Layer   | Layer 2           | Layer 3          |
| Used By | Switch            | Router           |
| Purpose | Identify Device   | Identify Network |
| Changes | Usually No        | Yes              |
| Example | AA:BB:CC:DD:EE:FF | 192.168.1.10     |

---

# Easy Way to Remember

```text
MAC -> Device Identity
IP  -> Network Identity
```

---

# Quick Revision

```text
MAC Address
- Physical Address
- Used by Switch
- Layer 2
- Identifies Device

IP Address
- Logical Address
- Used by Router
- Layer 3
- Identifies Network
```
# What Happens When We Type google.com in a Browser?

This process involves many concepts such as:

* DNS
* ARP
* TCP
* HTTP/HTTPS
* NAT
* Routing

---

# Step 1: Browser Checks Cache

The browser first checks whether it already knows the IP address of Google.

Example:

```text
google.com -> 142.250.xxx.xxx
```

If found, DNS lookup is skipped.

---

# Step 2: DNS Lookup

If the IP address is not available in cache, DNS is used.

```text
google.com
↓
142.250.xxx.xxx
```

DNS converts domain names into IP addresses.

---

# Step 3: Check Whether Google is in the Same Network

Suppose:

```text
Laptop IP = 192.168.1.10
Google IP = 142.250.xxx.xxx
```

Google is outside the local network.

Therefore, packets must be sent to the:

```text
Default Gateway (Router)
```

---

# Step 4: ARP Request

The laptop knows the router's IP address:

```text
192.168.1.1
```

but it does not know the router's MAC address.

So the laptop sends:

```text
Who has 192.168.1.1 ?
Tell 192.168.1.10
```

Router replies:

```text
192.168.1.1 is at AA-AA-AA
```

Now the laptop knows the router's MAC address.

---

# Step 5: TCP 3-Way Handshake

Before sending data, TCP establishes a connection.

```text
Client -> SYN
Server -> SYN + ACK
Client -> ACK
```

Connection established.

---

# Step 6: HTTPS Request

The browser sends an HTTPS request to Google.

Example:

```text
GET /
Host: google.com
```

Usually this request is sent to:

```text
Port 443
```

---

# Step 7: NAT at Router

Inside the home network:

```text
Laptop IP = 192.168.1.10
```

This is a private IP address.

The router converts it into:

```text
49.xx.xx.xx
```

which is the public IP assigned by the ISP.

This process is called:

```text
NAT
```

---

# Step 8: Routing Across the Internet

The packet travels through multiple routers.

```text
Laptop
 ↓
Home Router
 ↓
ISP Router
 ↓
Internet Routers
 ↓
Google Server
```

Each router checks the destination IP address and forwards the packet to the next router.

---

# Step 9: Google Server Processes the Request

Google receives the request:

```text
GET /
Host: google.com
```

and prepares the response.

Example:

```text
HTML
CSS
JavaScript
Images
```

---

# Step 10: Response Travels Back

The response follows the reverse path:

```text
Google Server
 ↓
Internet Routers
 ↓
ISP Router
 ↓
Home Router
 ↓
Laptop
```

---

# Step 11: Reverse NAT

The router receives packets for:

```text
49.xx.xx.xx
```

Router checks the NAT table:

```text
49.xx.xx.xx:6001
↓
192.168.1.10:5001
```

and forwards the packets to the laptop.

---

# Step 12: Browser Renders the Page

The browser receives:

* HTML
* CSS
* JavaScript
* Images

and displays the Google homepage on the screen.

---

# Complete Flow

```text
Browser Cache
     ↓
DNS Lookup
     ↓
ARP
     ↓
TCP 3-Way Handshake
     ↓
HTTPS Request
     ↓
NAT
     ↓
Routing
     ↓
Google Server
     ↓
Response
     ↓
Reverse NAT
     ↓
Browser Rendering
```

---

# Easy Way to Remember

```text
DNS
↓
ARP
↓
TCP Handshake
↓
HTTPS Request
↓
NAT
↓
Routing
↓
Response
↓
Browser Rendering
```

---

# Quick Revision

```text
1. Browser Cache Check
2. DNS converts domain name to IP.
3. ARP finds router MAC address.
4. TCP connection is established.
5. HTTPS request is sent.
6. NAT converts private IP to public IP.
7. Routers forward packets.
8. Google processes the request.
9. Response comes back.
10. Browser renders the page.
```
# Data Link Layer (Layer 2)

The Data Link Layer is responsible for:

```text
Node to Node Delivery
```

which means communication between two devices in the same network.

---

# Example

Suppose we have:

```text
Laptop A
IP  = 192.168.1.10
MAC = AA-AA-AA

Laptop B
IP  = 192.168.1.20
MAC = BB-BB-BB
```

Both devices are connected through a switch.

```text
Laptop A
    |
  Switch
    |
Laptop B
```

Laptop A wants to send data to Laptop B.

Network Layer identifies:

```text
Destination IP = 192.168.1.20
```

Data Link Layer identifies:

```text
Destination MAC = BB-BB-BB
```

The switch then forwards the frame to Laptop B.

---

# Why do we need Data Link Layer?

Think of sending a letter.

```text
City Address  -> IP Address
House Number  -> MAC Address
```

IP Address helps to find the correct network.

MAC Address helps to find the correct device inside that network.

---

# Data Unit of Data Link Layer

| Layer           | Data Unit |
| --------------- | --------- |
| Transport Layer | Segment   |
| Network Layer   | Packet    |
| Data Link Layer | Frame     |
| Physical Layer  | Bits      |

Data Link Layer sends data in the form of:

```text
Frames
```

---

# Frame

The Data Link Layer adds:

* Source MAC Address
* Destination MAC Address
* Error Detection Information

Example:

```text
+------------------------------------------------+
| Source MAC | Destination MAC | Data | CRC |
+------------------------------------------------+
```

This complete structure is called a:

```text
Frame
```

---

# Error Detection

Suppose during transmission:

```text
10110101
```

becomes:

```text
10100101
```

because of noise in the channel.

The Data Link Layer detects this error using:

```text
CRC (Cyclic Redundancy Check)
```

If an error is detected:

```text
Frame is discarded.
```

---

# MAC Address

Data Link Layer uses:

```text
MAC Address
```

for communication inside a local network.

Example:

```text
AA:BB:CC:DD:EE:FF
```

---

# Devices Working at Data Link Layer

The main device working at this layer is:

```text
Switch
```

because it forwards frames using MAC addresses.

---

# Main Functions of Data Link Layer

## 1. Framing

Converts packets into frames.

---

## 2. Physical Addressing

Uses MAC addresses for communication.

---

## 3. Error Detection

Detects transmission errors using CRC.

---

## 4. Flow Control

Prevents a fast sender from overwhelming a slow receiver.

---

## 5. Access Control

Determines which device can use the communication channel.

---

# Easy Way to Remember

```text
Network Layer   -> Network to Network Delivery
Data Link Layer -> Node to Node Delivery
Physical Layer  -> Bit Transmission
```

---

# Quick Revision

```text
Layer          -> Layer 2
Data Unit      -> Frame
Address Used   -> MAC Address
Device Used    -> Switch
Delivery Type  -> Node to Node Delivery

Functions:
- Framing
- Physical Addressing
- Error Detection
- Flow Control
- Access Control
```


# Physical Layer (Layer 1)

Physical Layer is the lowest layer of the OSI model.

It is responsible for:

```text
Transmission of bits over the communication medium.
```

---

# What does Physical Layer do?

The Physical Layer sends:

```text
0s and 1s
```

from one device to another through cables or wireless signals.

Examples:

* Copper Cable
* Fiber Optic Cable
* WiFi
* Radio Waves

---

# Example

Suppose your laptop wants to send:

```text
Hello
```

Computers cannot understand text directly.

So it is converted into binary:

```text
01001000 01100101 01101100 01101100 01101111
```

The Physical Layer sends these bits through the communication medium.

---

# Data Unit of Physical Layer

The Physical Layer sends data in the form of:

```text
Bits
```

Example:

```text
10110101
```

---

# Transmission Media

## Guided Media

Signals travel through physical cables.

Examples:

* Twisted Pair Cable
* Coaxial Cable
* Fiber Optic Cable

---

## Unguided Media

Signals travel through air.

Examples:

* WiFi
* Bluetooth
* Radio Waves
* Infrared

---

# Devices Working at Physical Layer

The main devices are:

* Hub
* Repeater

---

## Hub

A Hub forwards incoming signals to all connected devices.

It does not understand:

* MAC Address
* IP Address

It only forwards electrical signals.

---

## Repeater

A Repeater regenerates weak signals.

Example:

```text
Long Distance
↓
Signal becomes weak
↓
Repeater strengthens signal
↓
Signal continues
```

---

# Main Functions of Physical Layer

## 1. Bit Transmission

Transmits bits from one device to another.

---

## 2. Encoding

Converts bits into electrical, optical, or radio signals.

Example:

```text
1 -> High Voltage
0 -> Low Voltage
```

---

## 3. Data Rate Control

Determines the speed of transmission.

Examples:

```text
100 Mbps
1 Gbps
10 Gbps
```

---

## 4. Physical Topology

Defines how devices are physically connected.

Examples:

* Bus Topology
* Star Topology
* Ring Topology

---

## 5. Transmission Mode

Defines the direction of communication.

Examples:

* Simplex
* Half Duplex
* Full Duplex

---

# Example of Communication Flow

```text
Application Layer
        ↓
Transport Layer
        ↓
Network Layer
        ↓
Data Link Layer
        ↓
Physical Layer
        ↓
Cable / WiFi
        ↓
Physical Layer
        ↓
Data Link Layer
        ↓
Network Layer
        ↓
Transport Layer
        ↓
Application Layer
```

---

# Easy Way to Remember

```text
Physical Layer  -> Bits
Data Link Layer -> Frames
Network Layer   -> Packets
Transport Layer -> Segments
```

---

# Quick Revision

```text
Layer        -> Layer 1
Data Unit    -> Bits
Devices      -> Hub, Repeater

Functions:
- Bit Transmission
- Encoding
- Data Rate Control
- Physical Topology
- Transmission Mode
```

# Network Topologies

Network Topology defines:

```text
How devices are connected in a network.
```

In simple words:

```text
Topology = Structure or Layout of a Network
```

---

# Bus Topology

In Bus Topology, all devices share a single cable called:

```text
Backbone Cable
```

Example:

```text
PC1 ---- PC2 ---- PC3 ---- PC4 ---- PC5
```

When one device sends data, all devices receive it, but only the intended receiver accepts it.

---

## Advantages

* Cheap
* Easy to install
* Requires less cable

---

## Disadvantages

* If the backbone cable fails, the entire network stops.
* Performance decreases as more devices are added.
* Difficult to troubleshoot.

---

# Star Topology

In Star Topology, all devices connect to a central device such as:

* Switch
* Hub

Example:

```text
        PC1
         |
PC2 --- Switch --- PC3
         |
        PC4
```

If PC1 wants to send data to PC3:

```text
PC1
 ↓
Switch
 ↓
PC3
```

---

## Advantages

* Easy to manage.
* Easy to add new devices.
* Failure of one cable affects only one device.
* Better performance.

---

## Disadvantages

* If the central device fails, the entire network stops.
* Requires more cable.

---

# Ring Topology

In Ring Topology, devices are connected in the form of a circle.

Example:

```text
PC1 --- PC2
 |       |
PC4 --- PC3
```

Data travels around the ring until it reaches the destination.

---

## Advantages

* No collisions.
* Predictable performance.

---

## Disadvantages

* Failure of one device may affect the entire network.
* Difficult to troubleshoot.

---

# Mesh Topology

In Mesh Topology, every device is connected directly to every other device.

Example:

```text
A ----- B
|\     /|
| \   / |
|  \ /  |
|  / \  |
| /   \ |
|/     \|
C ----- D
```

---

## Advantages

* Very reliable.
* Multiple paths exist between devices.
* Failure of one connection does not stop communication.

---

## Disadvantages

* Expensive.
* Requires many cables.
* Complex to manage.

---

# Tree Topology

Tree Topology is a combination of:

```text
Star + Bus
```

Example:

```text
           Router
             |
        -------------
        |           |
      Switch1    Switch2
      /   \       /   \
    PC1  PC2    PC3  PC4
```

---

## Advantages

* Easy to expand.
* Suitable for large organizations.

---

## Disadvantages

* Failure of the root device affects many devices.
* More complex than Star Topology.

---

# Comparison Table

| Topology | Main Idea              | Failure Impact                        |
| -------- | ---------------------- | ------------------------------------- |
| Bus      | Single Backbone Cable  | Entire network fails                  |
| Star     | Central Device         | Central device failure affects all    |
| Ring     | Circular Connection    | One failure may affect entire network |
| Mesh     | Multiple Connections   | Very reliable                         |
| Tree     | Hierarchical Structure | Root failure affects many devices     |

---

# Most Commonly Used Topology

```text
Star Topology
```

Modern LAN networks mostly use Star Topology because they use switches as the central device.

---

# Easy Way to Remember

```text
Bus   -> One Cable
Star  -> One Central Device
Ring  -> Circle
Mesh  -> Everyone Connected
Tree  -> Hierarchy
```

---

# Quick Revision

```text
Bus   -> Backbone Cable
Star  -> Switch/Hub at Center
Ring  -> Circular Connection
Mesh  -> Direct Connection Between All Devices
Tree  -> Combination of Star and Bus

Most Commonly Used:
Star Topology
```
