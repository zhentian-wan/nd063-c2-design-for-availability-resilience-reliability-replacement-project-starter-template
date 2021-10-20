### EC2 instance

```bash
ssh -i "udacity-new.pem" ec2-user@ec2-3-88-32-200.compute-1.amazonaws.com
sudo su
yum update -y
yum install mysql -y
```

```bash
mysql -u admin -p -h udacity.crzba8oefe5s.us-east-1.rds.amazonaws.com
```

SSH into secondary region

```bash
chmod 400 udacity-new2.pem
ssh -i "udacity-new2.pem" ec2-user@ec2-18-119-119-92.us-east-2.compute.amazonaws.com
mysql -u admin -p -h udacity.ctzd4ndyg8tg.us-east-2.rds.amazonaws.com
```

S3 policy

````

{
    "Version": "2012-10-17",
    "Id": "Policy1634716708050",
    "Statement": [
        {
            "Sid": "Stmt1634716704650",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::udacity-project-l1-zhentian-23452432/*"
        }
    ]
}
```

http://udacity-project-l1-zhentian-23452432.s3-website-us-east-1.amazonaws.com