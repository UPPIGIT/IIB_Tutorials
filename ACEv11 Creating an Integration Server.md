ACEv11 Creating an Integration Server
........................................
Step 1: Creating an Integration server

Create an Integration Server 
...............................................
1. Assuming you are using a Windows platform, open an App Connect Enterprise Command Console and start an integration server using the following command:
IntegrationServer --work-dir C:\MyServer --name MyServer --admin-rest-api 7600 --http-port-number 7900 --console-log 
where C:\MyServer is a folder on your file system that the server will use for its working directory. 

2. After a few seconds the server should report that it has finished initialization and that its HTTP Listener has started listening for connections. Well done, you've just created a standalone Integration Server hosted locally on your own machine! 

Create a second Integration Server which is owned by an Integration Node 
........................................................................
1. Open a new App Connect Enterprise Command Console and create an integration node using the following command:
mqsicreatebroker MyNode 

2. Start the Integration Node using the following command:
mqsistart MyNode

3. Create an Integration Server which is owned by the Integration Node using the following command:
mqsicreateexecutiongroup MyNode -e MyNodeOwnedServer

4. Make a note of the administration port which the Integration Node has opened using the mqsilist command.
The response should report something like:
BIP1325I: Integration node 'MyNode' with administration URI 'http://YourHostName:4414' is running.
