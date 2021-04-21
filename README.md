## PACKAGE INSTALL
```
sudo su -
yum install git wget epel-release unzip -y
yum install ansible python2-pip -y
pip install boto3
wget https://releases.hashicorp.com/terraform/0.12.29/terraform_0.12.29_linux_amd64.zip
unzip terraform*
mv terraform  /usr/bin
terraform -v
mkdir ~/.aws/
git clone https://github.com/john24rel/ansible-terraform-import-ec2.git
```
## only when using AWS_ACCESS_KEY_ID
## create a file called 
```
~/.aws/credentials
[mm]
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
```
## create a file called
```
~/.aws/credentials.sh
export AWS_ACCESS_KEY_ID=
export AWS_SECRET_ACCESS_KEY=
```
## PING HOST
```
ansible -i localhost or vm host -m ping
```
## RUN PLAYBOOk
```
ansible-playbook  terraform-import-ec2.yml 
```


