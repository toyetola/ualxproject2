RUN the commnad below FROM terminal to provison the infrastructure and lauch the application

The configuration files are:
final-project2.yml
final-project2.parameters.json

```
aws cloudformation create-stack --stack-name project2 --region us-east-1 --template-body file://final-project2.yml --parameters file://final-project2-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM"
```

To tear down the infrastructure run

```
aws cloudformation delete-stack --stack-name project2
```

To update RUN
```
aws cloudformation update-stack --stack-name project2 --region us-east-1 --template-body file://final-project2.yml --parameters file://final-project2-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --profile cfoperations
```