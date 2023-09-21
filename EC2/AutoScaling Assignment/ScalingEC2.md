# Building Scalable application with AWS EC2

## Implementing High Availability and Scalability with AWS EC2, Elastic Load Balancer, and Auto Scaling Groups

### Steps

1. Create 2 Subnets and auto assign Public IPv4 Address 

![Subnets](S1.png)

2. Launch a Template

![Template](LT1.png)

3. Creating a Target Group

![Target Group](TG1.png)

4. Creating a Load Balancer

![Load Balancer](LB.png)

5. Creating a Auto Scaling Group

![Auto Scaling Group](ASG.png)

6. Auto Scaling Group Launched 2 Instances with Instance State Running

![EC2 Instances](Instances.png)

7. Navigate to Target Group Section and Check whether 2 Instances are healthy

![Checking Instances](TGCheck.png)

8. Navigate to Load Balancer Section and Copy the DNS URL and paste in new browser tab
   ### It will display one the instance id
![InstanceId1](I1.png)

   ### Reload the url and it will display another instance id

![InstanceId2](I2.png)


