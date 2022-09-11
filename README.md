# AMI_Load-balancing_SSH_with_Session-Manager_EC2-user-data-scripts
AMI, LOAD BALANCING, SSH WITH SESSION MANGER, EC2 USER DATA SCRIPTS

AMI, LOAD BALANCING, SSH WITH SESSION MANGER, EC2 USER DATA SCRIPTS

For s3 to be able to communicate with ec2 we need a role.
Steps to create a role:
    • First create a role, a role allows a service in AWS communicate with another.
    • Go to the IAM console
    • Select roles and select create role
    • Name the role you want to create
    • Attach policy to the role such as s3fullacess and SSM policy
    • Review and Create

Create your s3 bucket
To create an s3 bucket:
    • Search s3 in the AWS services
    • Select s3 and Create bucket.
    • Name the bucket
    • Assign a region and uncheck “block all public access” for the website to the publicly accessible.
    • Enable server-side encryption.
    • Disable static website hosting.
    • After configuring settings, upload source codes.

Launch an instance/ec2 and creating AMI
    • Search ec2 in the all services in the management console
    • Select launch instance
    • Configure instance setting like the network, OS, Storage, Tags and Security Group
    • Launch instance
    • Launch website
    • On the left side of the page, find AMI
    • Select AMI to see instances running
    • Select the instance, Choose Action
    • In the pop up button, select image and create.
    • Go back to the instance to find an image of your server running 

Create a Load balancer to allow an even distribution of network traffic.
Steps to create a load balancer:
    • On the ec2 page, find load balancer at the left side 
    • Select create load balancer
    • Configure setting like the availability zone, network security, network protocols, target groups
    • Name your target group and add protocols
    • Register Target
    • Add the two severs to the load balancer
    • Review settings and create.
    • Launch the website

To start a session,
    • Go to AWS System Manager
    • Select a session manager
    • Use data scripts to edits a text in the website
    • Reload to see changes made in the website
