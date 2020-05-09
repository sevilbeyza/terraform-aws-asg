# terraform-aws-asg
This Module for creating AutoScaling Group 
it is softcoded resuable for every region.

How Auto Scaling Group works
script creates an Auto Scaling Group to make architecture Highly Available and in order that our WordPress application will not down even one of our instances will be stopped or terminated (use module-ec2_as). 

We need to configure it to use the Launch Configuration we previously created. Within the boundaries that we define, AWS will launch instances into the ASG dynamically based on the current load across all instances. Equally when the load drops, some instances will be terminated accordingly. 

Exactly how many instances are launched or terminated is defined in one or more scaling policies, which are also created and linked to the ASG. The minimum and maximum sizes for the auto scaling group are can be set to 3 and 48 respectively. 

It's important to get these values right for your application workload. You do not want to be under resourced for early peaks in traffic, and for redundancy reasons it's a good idea to always have at least 3 instances in service. 

Equally you probably want your application to scale for peak periods, but perhaps not beyond a safety limit in the event you receive massive amounts of traffic which could result in escalating costs.
