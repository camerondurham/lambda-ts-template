# readme

From https://docs.aws.amazon.com/lambda/latest/dg/typescript-package.html

## deploying

```sh
npm run build
```

creating lambda function:

```sh
aws lambda create-function --function-name hello-world --runtime "nodejs16.x" --role arn:aws:iam::123456789012:role/lambda-ex --zip-file "fileb://dist/index.zip" --handler index.handler
```

how to create lambda execution role: https://docs.aws.amazon.com/lambda/latest/dg/lambda-intro-execution-role.html

update function code:

```sh
    aws lambda update-function-code \
              --function-name  hello-world \
              --zip-file "fileb://dist/index.zip"
```
