# serverless-deploy-workflow
AWS で CloudFront x Lambda@Edge の構成と GitHub Actions でデプロイできるテンプレート

SECRETS
SLS_INTERACTIVE_SETUP_ENABLE=1

現状は、serverless 2.72.2 を使用しないと、
npm install -g yarn serverless@2.72.2
以下のようなエラーが出る。
```
Run serverless deploy
Serverless Components CLI v1 is no longer bundled with Serverless Framework CLI
To run it, ensure it's installed:
npm install -g @serverless/cli
Then run:
components-v1 <command> <options>
```
まだ解決はされていない。
https://github.com/serverless-nextjs/serverless-next.js/issues/2320
