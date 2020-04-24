ACEv11 Creating an Integration Node
......................................

ACEv11 Creating an Integration Node

 
In continuation with previous blog entry, below steps contain details about creating an Integration Node in ACE v11.

Step 1: Create a Integration Server which is owned by an Integration Node
1. Open a new App Connect Enterprise Command Console and create an integration node using the following command:
mqsicreatebroker MyNode1

2. Start the Integration Node using the following command:
mqsistart MyNode1

3. Create an Integration Server which is owned by the Integration Node using the following command:
mqsicreateexecutiongroup MyNode1 -e MyNodeIntServer1

4. Make a note of the administration port which the Integration Node has opened using the mqsilist command.
MyNode1 http://localhost:4419

 

Step 2: Connect to the Integration Node MyNode
1. Still in the Integration Explorer view in the ACE Toolkit, right click on the Integration Nodes label and select Connect to an Integration Node

2. Enter the Host Name as localhost and the port number which was reported to you using the mqsilist command which we ran in Step 1.

3. Your node labelled MyNode1, and its server labelled MyNodeIntServer1 should appear with green arrows showing that they are currently running.