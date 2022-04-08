### [System Design Basics: Horizontal vs. Vertical Scaling](https://youtu.be/xpDnVSmNFX0)
Horizontal Scaling  
Vertical Scaling

|Horizontal Scaling|Vertical Scaling|
|-|-|
|Load Balancing Required|<u>N/A</u>|
|<u>Resilient</u>|Single Point of Failure|
|Network calls (RPC)|<u>Inter Process Communication</u>|
|Data Inconsistency|<u>Consitent</u>|   
|<u>Scale well as users increase</u>|Hardware limit|

### Reference  
- **RPC**: In distributed computing, a **remote procedure call (RPC)** is when a computer program causes a procedure (subroutine) to execute in a different address space (commonly on another computer on a shared network), which is coded as if it were a normal (local) procedure call, without the programmer explicitly coding the details for the remote interaction.  
RPCs are a form of inter-process communication (IPC)
- **IPC**: In computer science, **inter-process communication or interprocess communication (IPC)** refers specifically to the mechanisms an operating system provides to allow the processes to manage shared data. Typically, applications can use IPC, categorized as clients and servers, where the client requests data and the server responds to client requests. Many applications are both clients and servers, as commonly seen in distributed computing.