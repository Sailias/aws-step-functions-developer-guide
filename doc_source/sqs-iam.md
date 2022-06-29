# Amazon Simple Queue Service<a name="sqs-iam"></a>

These example templates show how AWS Step Functions generates IAM policies based on the resources in your state machine definition\. For more information, see:
+ [IAM Policies for integrated services](service-integration-iam-templates.md)
+ [Service Integration Patterns](connect-to-resource.md)

*Static resources*

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "sqs:SendMessage"
            ],
            "Resource": [
                "arn:aws:sqs:[[region]]:[[accountId]]:[[queueName]]"
            ]
        }
    ]
}
```

*Dynamic resources*

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "sqs:SendMessage"
            ],
            "Resource": "*"
        }
    ]
}
```