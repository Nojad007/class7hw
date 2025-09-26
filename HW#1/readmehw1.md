# To create an EC2 with a security group:

# 1 - Search for EC2 in the search bar and in the left menu click on 'Security Groups".
# 2 - Click on the orange button on the right of the screen to start a security group
# 3 - Type in the name for your security group and put in a description 
# 4 - Scroll down to 'Inbound Rules' and search for 'HTTP' in the first drop down menu. The protocol and port is already set for you. in the next open space to the right, change the IP range to 0.0.0.0/0, which is an IP to allow all incoming traffic. Add a description in the final space on the far right, then, click the orange button at the bottom. If you see a green banner then the group has been made
# 5 - Go back to the EC2 screen. On the left hand side, click on 'Instances'. Then click on the orange button on the right
# 6 - Name the instance in the first space at the top
# 7 - Scroll all the way down to 'Key Pair' and in the drop down, select 'Proceed With A Key Pair'
# 8 - Scroll down to 'Network Settings'. Make sure 'Auto-assign public IP'is set to 'Enable'. 
# 9 - Click on 'Select Existing Security Group' and in the drop down menu below, select the group you made
# 10 - Scroll all the way down to the 'Advanced Details'. Open the drop down menu and scroll down to 'User Data'. Paste in your script of choice, then click the orange button on the far right.
# 11 - Once the instance is showing green checks under 'Instance State' and 'Status Check' then the instance has been made. Click the check box for this instance, copy the 'Public DNS and open a new browser tab. Type in http:// and paste in the Public DNS. The web server page should open






# To Break down the entire process:

# In the instance section, under 'Instance State', Click the drop down menu and select 'Terminate Instance'.
