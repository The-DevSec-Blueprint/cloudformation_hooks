# Stop Your Developers from Creating Noncompliant Resources with AWS CloudFormation Hooks

## Notes to call out

1. Hooks have to be activated in each region for your resources. :sad

## Deploying Template

1. aws cloudformation deploy --stack-name <stack_name> --template-file <stackfile_name> 
>**NOTE**: Add -capabilities CAPABILITY_NAMED_IAM for IAM role deployment
2. aws cloudformation delete-stack --stack-name <name_of_stack>

## Hook Configuration

```json
{
    "CloudFormationConfiguration": {
        "HookConfiguration": {
            "TargetStacks":"ALL",
            "FailureMode":"FAIL"
        }
    }
}
```

## Notes for development purposes

AwsCommunity::EC2::SecurityGroupRestrictedSSH - Remember this!

## Resources Used - Research

- https://docs.aws.amazon.com/cloudformation-cli/latest/hooks-userguide/what-is-cloudformation-hooks.html
- [CloudFormation Hook 101](https://dev.to/aws-builders/cloudformation-hook-101-3jmj#config)
