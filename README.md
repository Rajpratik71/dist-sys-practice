# Distributed Systems Practice

Notes from learning about distributed systems in [GW CS 6421](https://gwdistsys18.github.io/) with [Prof. Wood](https://faculty.cs.gwu.edu/timwood/)

## Area 1: Cloud Web Apps

> Beginner Level

[AWS Tutorial: Launch a VM](https://aws.amazon.com/getting-started/tutorials/launch-a-virtual-machine/) (time: 30 min)

Notes: In this lecture, I have learned how to lauch, configure, connect, and terminate an instance in the cloud. Besides, I have learned 2 linux commands:  `chmod` and `ssh` :

- chmod xxx filename . Change the access permissions, **ch**ange **mod**e. 3 digits stand for: user, group, and world. 4 means read, 2 means write, 1 means execute.

```
chmod 400 file.txt    // allow read by owner
chmod 740 file.txt     // allow read, write, execute by owner, allow read by group
chmod 777 file.txt    // allow everyone to read, write, and execute file
```

- ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine.

```
ssh -i file [user@]hostname    // here, -i means selecting a file from which the identity for RSA is read.
```

[QwikLab: Intro to S3](https://awseducate.qwiklabs.com/focuses/30?parent=catalog) (time: 25 min)

Notes: In this lab, I learned the basic usage of **S3** by finishing the tasks one by one. Amazon Simple Storage Service (Amazon S3) is storage for the Internet. Users can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere on the web. Following the instructions, I have created a bucket in S3, added 2 pictures to my bucket, managed access permisson on pictures, created a Bucket Policy for permisson control, and tried to use bucked versioning.

> Intermediate Level

[Video: Virtualization](https://www.youtube.com/watch?v=GIdVRB5yNsk) (time: 20 min)

[AWS Tutorial: Install a LAMP Web Server on Amazon Linux 2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-lamp-amazon-linux-2.html) (time: 45min)

In this practice, I learned how to install a **Lamp Web Server** on amazon Linux 2 by installing an Apache web server with PHP and MariaDB (a community-developed fork of MySQL) . We can use this server to host a static website or deploy a dynamic PHP application that reads and writes information to a database.

The first step is to prepare and lauch LAMP Server. When finishing connecting to the EC2 instance via SSH, we need to install the latest version of the LAMP MariaDB and PHP packages for Amazon Linux 2, then use **yum install** commond to install multiple software packages and related dependencies (such as httpd, mariadb-server). After that, we start the Apache webserver via `sudo systemctl start httpd` command. By the way, to test the web server in the web browser, we need to first add a security rule to allow inbound HTTP (port 80) to the instance, then type the public DNS address of the instance on browser, we can see the Apache test page. Besides, setting file permission inside `/var/www/html` to ensure we can add, delete, and edit files in the Apache document root.

The second step is to test the LAMP Server via creating a PHP file in the Apache document root. We use `echo` command to write something into a file. By entering the public DNS address plus the file address, we can see the webpage on the web browser.

The second step is to secure the database server because the default installation of the MariaDB server should be disabled or removed for production servers.

[QwikLab: Intro to DynamoDB](https://awseducate.qwiklabs.com/focuses/23?parent=catalog) (time: 20min)

In this lecture, I learned about **Amazon DynamoDB**. It is a fast and flexible NoSQL database service. It's also a fully managed database and supports both document and key-value data models.

In this lecture, I tried to create a table in Amazon DynamoDB, and added and edited some data to it, then tried to query and search data from it, finally I deleted the table I created. All of the operations can be done on the console by mouse clicking.



[AWS Tutorial: Deploy a Scalable Node.js Web App](https://aws.amazon.com/getting-started/projects/deploy-nodejs-web-app/?trk=gs_card) (time: )

## Area 2

> Include notes here about each of the links
