# Basic Lambda Slack App

> [!CAUTION]
> ARM Architecture not supported yet! If you're a ARM(Mac, RaspberryPi ...) user, please try [Cloud9](https://us-east-1.console.aws.amazon.com/cloud9control/home) to deploy your slack app. (ARM 아키텍처는 아직 지원되지 않습니다. Mac, RaspberryPi 등의 ARM 기기를 사용하신다면 [Cloud9](https://us-east-1.console.aws.amazon.com/cloud9control/home)을 활용하여 slack app을 배포하시기 바랍니다.)

<br/>

# Used
- [Slack Bolt for Python](https://github.com/slackapi/bolt-python)
- [AWS CLI](https://aws.amazon.com/ko/cli/)
- [AWS SAMCLI](https://docs.aws.amazon.com/ko_kr/serverless-application-model/latest/developerguide/install-sam-cli.html#install-sam-cli-instructions)
- [Docker](https://docs.docker.com/engine/install/)

<br/>

# Project Structure
```
📦aws-cost-explorer-slack-app
 ┣ 📂src
 ┃ ┣ 📂listeners
 ┃ ┃ ┣ 📂handlers
 ┃ ┃ ┃ ┗ 📜meow.py
 ┃ ┃ ┗ 📜events.py
 ┃ ┣ 📜app.py
 ┃ ┗ 📜requirements.txt
 ┣ 📜.gitignore
 ┣ 📜README.md
 ┗ 📜template.yaml
```

# Deployment
```
# 1st Deployment
sam build -u & sam deploy --guided --capabilities CAPABILITY_NAMED_IAM

# Update
sam build -u & sam deploy --no-confirm-changeset --no-disable-rollback --capabilities CAPABILITY_NAMED_IAM
```