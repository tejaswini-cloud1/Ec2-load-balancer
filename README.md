# Ec2-load-balancer
Create an Application load balancer and attach the load balancer to Ec2 Instance 

Step 1: Create an EC2 Instance
Before attaching a load balancer, you must have at least one running EC2 instance. If you do not have an instance, you can create one using the AWS Management Console. Ensure that the instance is running and healthy before proceeding to the next step.

Step 2: Create a Load Balancer
Next, you need to create a load balancer using the AWS Management Console. Navigate to the EC2 dashboard and select “Load Balancers” from the left-side menu. Click on “Create Load Balancer” and follow the prompt to configure your load balancer. Ensure that you select the appropriate protocol and port for your application.
Select Load balancer types: Application Load Balancer
Enter your ELB name
In Network mapping, Select VPC if you have one, or you can leave it as the default option
In Network mapping, Select at least two Availability Zones
In Security groups, Create a new security group with an inbound rule for port 80 or select the default security group that already has an inbound rule for port 80.
In Listeners and routing, Create new target group (target type must be “instance”, enter the name of your target group, select your VPC if applicable, and leave the remaining fields as they are and click on next)
Select the instance that you wish to attach to the ELB and Click on `Include as pending below` button. And then Create target group
 In Listeners and routing, After creating the target group, make sure to add it.
 And leave the remaining fields as they are, click on the Create button, and patiently wait for a few minutes for the provisioning process to complete.
 Step 3: Test the Load Balancer
After registering the instance, you can test the load balancer to ensure that it is working properly. Navigate to the load balancer’s DNS name in a web browser, and you should see your application running. If the load balancer is not working, you can troubleshoot any issues using the AWS Management Console.
Conclusion:-
Attaching load balancers to EC2 instances is a critical step in ensuring that your applications can handle high amounts of traffic. With this step-by-step guide, you should now be able to create and configure load balancers on AWS with ease.
