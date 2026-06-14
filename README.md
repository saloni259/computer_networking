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