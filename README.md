# Stop Your Developers from Creating Noncompliant Resources with AWS CloudFormation Hooks

![]() - Put Video Thumbnail here - make it clickable

Hello everyone! Thanks for checking out this project. If you have any questions, don't hesitate to reach out to me!

## CloudFormation Template Commands

In the video, there is one command that I use for deploying the CloudFormation template stack into my AWS account using the AWS CLI. The command is highlighted below:
```shell
$ aws cloudformation deploy --stack-name <replace_me> --template-file <replace_me> 
```
>**NOTE**: Add -capabilities CAPABILITY_NAMED_IAM for IAM role deployment

To clean up your stack, enter the following command:

```shell
$ aws cloudformation delete-stack --stack-name <name_of_stack>
```

## CloudFormation Hook Type Configuration

When you get to the part where you're about to activate the AWSEC2Community