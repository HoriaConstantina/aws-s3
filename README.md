### How to set up an AWS S3 Bucket

- create an EC2 instance
- ssh into your newly created EC2 instance
- after you are inside your vm do the following:
	- sudo apt-get update
	- sudo apt-get upgrade
	- sudo apt-get install python
	- sudo apt-get install python-pip
	- sudo apt-get install awscli
	- aws configure:
		- Add your Access Key ID
		- Add your Secret access key
		- Add the location as: eu-west-1
		- Add the output as: json
	
	- After you have completed the configuration do the following:
		- aws s3 ls -> To show all the buckets available inside the S3 service
		- aws s3 mb s3://devops-bootcamp-yourName-bucket -> To create a bucket inside the S3 service
		- nano devops_bootcamp_test.txt -> To create a file
		- aws s3 cp devops_bootcamp_test.txt s3://devops-bootcamp-yourName-bucket -> To copy the file from your localhost inside your S3 bucket
		- rm -rf devops_bootcamp_test.text -> To remove the file from your localhost
		- aws s3 sync s3://devops-bootcamp-yourName-bucket/ devops_bootcamp_test.txt -> To download the file from your S3 bucket inside your localhost
		- aws s3 rm s3://devops-bootcamp-yourName-bucket/devops_bootcamp_test.txt -> To remove the file from your S3 bucket
		- aws s3 rb s3://devops-bootcamp-yourName-bucket -> To remove the bucket from the S3 service
	
	- To grant permissions to a file go inside your S3 bucket, click on your file, click on Object actions and select Make public

