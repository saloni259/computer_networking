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



