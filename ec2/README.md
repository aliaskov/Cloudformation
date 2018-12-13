## About
This template creates an EC2 instance, based on ECS optimized Amazon Linux with
git, aws cli, certbot (for ssl certs) docker-compose and s3-fs.

## Features:

1) EBS DataVolume with type and size parameters, automatically mounted on /opt/$STACKNAME directory
2) Elastic IP, Route53 A RecordSet of Elastic IP
3) S3 bucket, with s3fs mount on /opt/s3 directory, that gives opportunity to use S3 bucket as filesystem
4) docker and docker-compose installed and ready to use
5) letsencrypt Certbot project git cloned, to obtain free ssl certs easy and fast (git clone any other project)

## Before usage:
# Important!
### Replace word UnhappyDummy in CF template with your stack name.
## Use First Letter Capital!
```Example
Ctrl + F UnhappyDummy and replace with MyStackName.
```
## Usage
Open AWS console, CloudFormation, Create stack, Upload a template to Amazon S3, choose this template.
Specify a stack name and parameter values.
## Important!
# Stack name - LOWER CASE!!!

HTTPSLocation
 The IP address range that can be used to SSH to the EC2 instances

AppPort
 The IP address range that can be used to use http AND https to the EC2 instances
 The Application port that can be opened for a range of IPs

AppPortLocation
 The IP address range that can be used to use The Application port

InstanceType
 Choose Instance type
Domain

 Route53 Domain that serves as HostedZone for Route53. Provide a valid domain name using only lowercase letters
VolumeSize
 UnhappyDummy Data Volume size mounted on /opt in Gb
VolumeType
 UnhappyDummy /opt Data Volume type. Can be gp2 for General Purpose SSD, io1 for Provisioned IOPS SSD, st1 for Throughput Optimized HDD, sc1 for Cold HDD, or standard for Magnetic volumes.
