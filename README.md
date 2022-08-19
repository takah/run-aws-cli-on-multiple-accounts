# Run AWS CLI command on multiple accounts

## Usage
```
$ run-aws-cli-on-multiple-acconts -r administrator -c "lambda list-functions" -j ".Functions[] | {name: .FunctionName, runtime: .Runtime}" -R ap-northeast-1
```

## Configuration file: ~/.aws/assume-role.conf
```
account1 arn:aws:iam::012345678901:role/xxxxxx-role
account1 arn:aws:iam::012345678901:role/yyyyyy-role
account1 arn:aws:iam::012345678901:role/zzzzzz-role
account2 arn:aws:iam::123456789012:role/abcdef-role
account3 arn:aws:iam::987654321098:role/opqrst-role
```

## Funding
This work is funded by [Linkbal Inc.](https://linkbal.co.jp/)
