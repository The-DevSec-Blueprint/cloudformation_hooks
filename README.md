# Stop Your Developers from Creating Noncompliant Resources with AWS CloudFormation Hooks

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

## Resources Used - Research

- [CloudFormation Hook 101](https://dev.to/aws-builders/cloudformation-hook-101-3jmj#config)
