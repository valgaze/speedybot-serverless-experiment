## Speedybot Serverless POC

## Get AWS Credentials

See this video for details if you need access key & secret IDs: https://www.youtube.com/watch?v=D5_FHbdsjRc

## Setup Serverless Credentials on your machine

```sh
npm i -g serverless

serverless config credentials --provider aws --key mykey --secret secret

serverless config credentials --provider aws --key xxxx --secret yyyyy --profile speedybot_user

```

## Deploy

```sh
serverless deploy
```

Once deployed, you can find the url of your function with

```sh
serverless info
```

Once you have that, register your webhook with:

```sh
npx speedyhelper webhook register -t __REPLACE__ME__ -w https://aaabbbcccdddeee.execute-api.us-east-1.amazonaws.com

npx speedyhelper webhook remove -t __REPLACE__ME_ # remove all webhooks associated with token

npx speedyhelper webhook remove -t __REPLACE__ME_ -w https://aaabbbcccdddeee.execute-api.us-east-1.amazonaws.com # remove specific token
```
