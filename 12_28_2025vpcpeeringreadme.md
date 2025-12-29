<!-- Step-by-Step Guide to Set Up VPC Peering



Step 1: Identify the VPCs to Peer


You’ll need to know the details (VPC IDs, region, etc.) of the two VPCs you want to peer.
VPC 1 has CIDR 10.xxx.xxx.xxx/16
VPC 2 has CIDR 10.xxx.xxx.xxx/16
Make sure these CIDR blocks don’t overlap. Overlapping CIDR ranges will prevent successful peering.




Step 2: Create a VPC Peering Connection


Search for VPC click on 'Peering Connections'
Create a Peering Connection
Type in: name of the peering connection of your VPC, select your VPC ID, account ID (if you are connecting to another account), the region and then the VPC ID of VPC 2. 
The connection request is now pending and must be accepted by the other user(if on another account) or VPC (if on the same account)




Step 3: Accept the VPC Peering Connection (if the you're receiving the request)


Go to 'Peering Connections'
Go to the 'Actions' button and select 'Accept Request' 
This will establish the peering connection between both VPCs





Step 4: Update Route Tables


Navigate to 'Route Tables' under the VPC umbrella
Select the VPC you need and then click on 'Edit Routes'
Update the Route for VPC 1 by clicking on 'Add Route' and then enter the CIDR block of VPC 2
Next select 'Peering Connection' and then right below, the select the VPC ID created earlier
Make sure the route is updated for VPC 2 with the CIDR from VPC 1





Step 5: Update Security Groups


Both VPCs have their own security groups, which act as firewalls for controlling traffic.

Navigate to 'Security Groups' under the EC2 umbrella
Make sure there are incoming rules for VPC 2 CIDR block, SSH & ICMP Ping 


Step 6: Create an EC2

Name the EC2 instance
Make sure no key pair is added
Edit the 'Network Settings': Select the corret VPC, Make sure the 'Auto-Assign Public IP' is enabled
Select an 'Exisiting Security Group', which is the one created for VPC 1
Then launch the instance
Select the instance and then click 'Connect' 
Under 'EC2 Instance Connect', make sure 'Connect Using A Public IP' is selected then click 'Connect' at the bottom
Ping the other instance on VPC 2's IP