# serverless-deploy-workflow
https://github.com/serverless/serverless
https://github.com/serverless-nextjs/serverless-next.js

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

If you have issues deploying due to new serverless version, please try to pin to specific version e.g 2.72.2. See #2320 (comment)

[ALPHA - may be buggy] You may also deploy using npx @sls-next/serverless-patched (or serverless-patched if you installed it locally), which is a patched version of serverless that fixes a couple of issues by patching the underlying @serverless/cli: (1) Continuous "Deploying" messages being printed in non-interactive terminals (e.g CI output) that make it hard to debug, and (2) Handles silent Next.js build failures.

It's also recommended to add --debug flag to get more useful logs of what's happening behind the scenes.

🚫 Don't attempt to deploy by running serverless deploy, use only serverless
