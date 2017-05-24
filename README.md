AWS CloudFormation Practice Exercise
=======================

### Prerequisites:
 * AWS account with configured CLI tools. More information can be found here if you have not set them up: <br>
 1) Install: http://docs.aws.amazon.com/cli/latest/userguide/installing.html <br>
 2) Configure: http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html
 * A good understanding of AWS modules: VPC / EC2 / RDS / CloudFormation / S3

### Instructions:
This is a 1 hour practical exercise to test your AWS knowledge. You may use the internet and AWS documentation to compete this task. You are required to produce a CloudFormation template either in JSON or YAML (your preference) which satisfies the following requirements:
1. Starts an AWS Linux EC2 classic instance which is publicly available and has a fully working / started version of WordPress which can be download from here: https://wordpress.org/latest.tar.gz You will need to automate the configuration using the wp-config-sample.php inside the tar<b> (5 points) </b>

2. The Wordpress installation should be backed by a MYSQL database. <b> (5 points) </b> <br>Knowledge of incorporating RDS into your answer is work an extra <b> (5 points) </b>.

3. The template should take the following parameters: <b> (5 points) </b>
  * DatabaseName: (Type: String Default: wordpress)
  * DatabaseUser: (Type: String Default: wordpress)
  * DatabasePassword: (Type: String Default: w0rdpr355)

4. The instance public IP should be output after the template is sucessfully complete. <b> (2 points) </b>

#### SUBMIT YOUR TEMPLATE VIA EMAIL: SION@OSODEVOPS.IO
#### Hints & Tips:
- You can quickly validate your template using this command:<br>
`aws cloudformation validate-template --template-body file://sampletemplate.json`

- The template should need no manual intervention so you should make make use of AWS::CloudFormation::Init or Fn::Base64 to encode instance userdata.

- Make use of core unix tools (SED / AWK / JQ) where appropriate.
