![ec2-jenkins](assets/ec2-jenkins.png)

# Install Jenkins Server on AWS EC2
[![user][user_img]][user_url] ![markdown][markdown_img]

[user_img]:https://img.shields.io/badge/made%20by-mehmetcangulesci-7B535E.svg
[user_url]:https://github.com/mehmetcangulesci

[markdown_img]:https://img.shields.io/badge/made%20with-Markdown-1f425f.svg

## Description
[Jenkins](https://www.jenkins.io/) is a self-contained, open source automation server which can be used to automate all sorts of tasks related to building, testing, and delivering or deploying software.

In this tutorial, I will try to cover installation of one of the most popular CI/CD tool Jenkins on AWS EC2 instance.

## Install
First thing to do is setup an AWS EC2 Instance. Second one is to execute commands to be given on EC2 instance to run Jenkins Server.

For successfull setup, follow the all instructions in the video content below.

![tutorial](assets/setup-jenkins-on-ec2.gif)

### Commands

```bash
# Update packages
$ sudo yum update -y
```

```bash
# Install Java
$ sudo yum install java-1.8.0-openjdk-devel
```

```bash
# Add Jenkins repo to your yum repository
$ sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo
```

```bash
# Import a key file from Jenkins-CI
$ sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key
```

```bash
# Install Jenkins
$ sudo yum install jenkins -y
```

```bash
# Start and enable Jenkins service
$ sudo systemctl start jenkins
$ sudo systemctl enable jenkins
```

```bash
# Check Jenkins service status
$ sudo systemctl status jenkins
```

```bash
# Get the administrative password 
$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

## Contributor
<table>
  <tr>
    <td align="center">
    <a href="https://mehmetcangulesci.com">
        <img src="https://avatars2.githubusercontent.com/u/17083968?v=3" width="30px;" alt=""/>
        <br />
        <sub><b>Mehmetcan Güleşçi</b></sub>
    </a>
    </td>
  </tr>
</table>
