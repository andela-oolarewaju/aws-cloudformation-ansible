# AWS Cloudformation script with Ansible

Clone this repo: 

```git clone https://github.com/andela-oolarewaju/aws-cloudformation-ansible.git ```

Then:

```$ cd aws-cloudformation-ansible```

Create a ```vars.yml``` file and put the following credentials and variables like:
```
aws_access_key_id: YOURACCESSKEY
aws_secret_access_key: YOURSECRETKEY
s3_website_index_document: "YOURINDEXFILE.html"
s3_website_error_document: "YOURERRORFILE.html"
s3_website_domain: "BUCKETNAME"
launch_cfg_name: "LAUNCHCONFIGNAME"

#for aws configure
output: "json"
region: "REGION"

instance_type: "INSTANCETYPE"
autoscaling_grp: "AUTOSCALINGGROUPNAME"
ami_name: "AMI-NAME"
cloudformation_name: "CLOUDFORMATIONSTACK-NAME"
bucket_name: "orezi-bucket"

#for cloudformation template
vpc_name: "VPCNAME"
public_subnet: "PUBLICSUBNET"
private_subnet: "PRIVATESUBNET"
internet_gw: "INTERNETGATEWAY"
gateway_to_internet: "GATEWAYTOINTERNET"
public_rt: "PUBLICROUTETABLE"
public_route: "PUBLICROUTE"
rt_association: "PUBLICROUTETABLEASSOCIATION"
private_instance: "PRIVATEINSTANCENAME"
instance_type: "INSTANCETYPE"
image_id: "ami-YOURID"
vpc_cidr_block: "VPCCIDRBLOCK"
public_sub_cidr: "PUBLICSUBNETCIDRBLOCK"
private_sub_cidr: "PRIVATESUBNETCIDRBLOCK"
pub_sub_1_zone: "zoneA"
pub_sub_2_zone: "zoneB"
load_balancer: "LOADBALANCER"
load_balancer_port: "PORT"
instance_port: "INSTANCE PORT"
protocol: "PROTOCOL"
crosszone: true
loadbalancername: "LOADBALANCER"
sns_name: "TOPIC"
sns_endpoint: "EMAIL"
sns_protocol: ""
min_size: ""
max_size: ""
desired_capacity: ""
```

This file **SHOULD NOT** be public

**RUN** `ansible-playbook playbook.yml -f 10`

**TO TEST**
cd into features/install.steps.rb

Fill in the variable values in the install.steps.rb file. example:
cloudformation_stack_name = ""
key_value = ""
ami_name = ""

**Then RUN** cucumber featuers/install.feature