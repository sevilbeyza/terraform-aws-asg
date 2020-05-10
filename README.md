terraform-aws-asg

For Aws provider a module to create Auto Scaling Group and Elastic Load Balancer

module "app1" { 
source = "./module"
region =  "us-west-2"
key_name = "Terraform_module"
image_owner = "137112412989"
desired_capacity = 1
max_size         = 1
min_size         = 1
} 






Terraform will perform the following actions when you apply:

  + module.app1.aws_autoscaling_attachment.asg_attachment_bar
  + module.app1.aws_autoscaling_group.example
  + module.app1.aws_elb.bar
  + module.app1.aws_key_pair.asg-key
  + module.app1.aws_launch_template.example
  + module.app1.aws_security_group.asg-sec-group
   
Plan: 6 to add, 0 to change, 0 to destroy.