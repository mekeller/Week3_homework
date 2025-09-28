Read me instructions on how to launch an EC2 with teardown instructions.



1. Create a security group.
2. Launch EC2 instance.
3. Tear down EC2 instance.





1. Create a security group.

* Click EC2. Scroll down to the "Network and Security" section and click "Security Groups"
* Click the orange button "Create security group"
* In the "Basic details" section, create a custom name in the "Security group name" field. Copy the custom name you placed in the "Security group name" field and put it in the "Description" field.
* Go to "Inbound Rules" section.
* Click "Add rule"
* Under the "type" field, select "HTTP". Under the "Source" field, select "Anywhere-IPv4". Under the "Description-optional" field, create a custom name for the field. It can be anything.
* DO NOT TOUCH OUTBOUND RULES. SKIP OVER THIS SECTION.
* Under "Tags-optional" section, you can create a key and value. In the "Key" field, create a custom key. In the "Value-optional" field, create a custom value. The key and value are custom identifiers to help you track certain things.
* Click the orange button "Create security group"



2\. Launch EC2 instance.

* Click EC2. Scroll down to the "Instances" section and click "Instances".
* Click the orange button "Launch instances".
* Under "Name and tags" section, in the "Name" field, create a custom instance name.
* In the "Key pair (login)" section, select "create new key pair".
* In the "key pair name" field, create a custom key pair. Once you create a name, click the orange button "Create  key pair".
* Under the "Network setting" section, scroll to "Firewall (security groups)", and select "Select and existing security group". Under the "Common security groups" field, click "Select security groups". Search for the security group that was initially created and select it. It should now be shown.
* Scroll to the "Advanced details" section, and scroll all the way down to "User data-optional". 
* Open a new browser screen and go to the GitHub link, https://github.com/MookieWAF/bmc4/blob/main/ec2scrpit
* On the right side of the screen and locate the double squares by "Raw" to "copy raw file". Click the double squares.
* Go back to your instance EC2 screen and paste the script from GitHub into the "User data-optional" field.
* Click the orange button "Launch instance".
* Click EC2. Go to the "Instances" section and click "Instances". You should now see your instance running by locating the instance you named and looking in the "instance state" section with green words and a check mark that says "running".
* In the "Details" section, locate "Public DNS", and click the double squares. Open a new browser tab and type "http://" and paste the link. You should now see your page live.





3\. Tear down EC2 instance.

* Click EC2. Scroll to the "Instances" section, and click "Instances".
* Locate the "Name" field, which will have the name of your instance you created. Click the box to highlight the instance.
* Click the blue bubble named "Instance state" and select "Terminate (delete) instance". A small window will pop up named "Terminate (delete) instance". Click the orange button "Terminate (delete)".
* In the "Instance state" section, it previously showed a green check mark with green words "running", but it should now read in grey words "Shutting-down". Give it a minute and it should now in grey words say "Terminated". 







































