## Lab 0: Making Connections...
### Introduction to the lab space
The purpose of lab 0 is to familiarize yourself with the lab space we will be
using for the remainder of the labs.  You should have received an email
regarding your AWS Educate account for this class.  We will be using AWS to
create virtual environments for you to use to complete the tasks given.

### A Note on Ethics

### Objectives
1. Become familiar with creating lab environments via AWS CloudFormation files
3. Brush up on a few networking topics needed for this course
2. Start building your git(hub) toolbox

### Background
There are all sorts of useful tools to scan, sniff, crawl, hack, crack, and
otherwise pwn a network but all of them are useless if you don't know how to
connect to it.  In this lab you will be making a simple connection to your AWS
environment using a tool called SSH.  You will then investigate advanced
connection techniques such as tunnels, proxies, and reverse shells.

### Resources and Setup

##### Resources
* This Github repository (/code)
* AWS Educate Environment

##### Setup
* Register for an account at https://github.com/
* Complete The AWS Educate Registration
* Create a Fork of this repository so you have it for your records
* Install Python 2.7, I recommend using [Anaconda Python](https://www.anaconda.com/distribution/)

###### Windows Only Setup
We are going to be making many connections to linux servers via SSH, some will
even have graphical applications that we will be accessing locally.  To do this
you will need an SSH client and local X server.  There are many options out
there and you are free to use whichever one you want; however, we will only be
supporting the following environment (which I would recommend trying out, if you
have a better suggestion send it to Matt Kijowski via Lab Talk).

* [Install Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
* Install Ubuntu 18.04 LTS from the Windows store
* Launch Ubuntu 18.04 LTS Bash to finish configuring your account
  (username/password)
* [Install MobaXterm Home Edition](https://mobaxterm.mobatek.net/download.html)


### Task 1 Provision the lab environment in AWS.  
Assuming you have registerd for AWS Educate and have access to this class you 
simply need to [sign in to AWS educate](https://www.awseducate.com/signin/SiteLogin),
go to the CEG 4900/6900 Cyber Security Analysis - Applied classroom, then click
the blue AWS Console button.  This will launch the AWS console (may require two
clicks if you were laready signed in to AWS with your personal account) and sign
you in as a federated user with a username looking like
`vocstartsoft/user236529=lastname.number@wright.edu`.

After successfully signing in you will first need to create and SSH key pair via
AWS for signing in to your systems.  To do this select the [EC2 service from the
AWS console](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Home:).
In the center area you should see a list of all Resources you have
available (you will be returning here often).  Right now they should all be 0.
Click on [0 Key Pairs](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#KeyPairs:sort=keyName)
From here you should see no existing SSH key pairs.  To create one click on the
`Create Key Pair` blue button.  This will create a public/private key pair,
stores the public key in AWS, and downloads the private key to your local
machine.  Do not lose this private key.  Doing so will prevent you from being
able to access any labs created with it.  If you do lose it simply delete it
from AWS and create a new one.

[Once you have created your SSH key, click here to provision lab0](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=CEG-4900Lab0&templateURL=https:%2F%2Fs3.amazonaws.com%2Fcf-templates-wylc6d3bougs-us-east-1%2Flab0.yml)
This will take you to another AWS service called Cloud Formation (AWS CF).  The
link will automatically fill most of the fields necessary, you will need to
select the SSH key you just created from the drop down menu.  After selecting
your key keep clicking next to finalize creation of your lab space.

Once you have created the AWS Cloud formation stack you can [return to the EC2
service](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Home:).
Here you should see additional resources have been created. [Click on Running
Instances](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Instances:sort=instanceState)
to see information about the servers created as a part of the cloud formation
template.  You will need to retrieve the Elastic IP of the Ubuntu instance by
selecting it and looking at the information in the Description below.

Finally, you are ready to make an SSH connection to your AWS server.  Using MobaXterm run the following


### Task 2


### Task 3


### Task 4


### Acknowledgement
Portions of this lab were derived from Black Hat Python: Python Programming for
HAckers and Pentesters, by Justin Seitz.
