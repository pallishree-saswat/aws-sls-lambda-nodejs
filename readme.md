Serverless Framework
npm install -g serverless -- in terminal as administrator

--> It will install a CLI for you in Ypour machine
--> type serverless or sls command to see other commands or features

Create a serverless project

serverless create -template or -t project-name
ex-:
serverless create -t myfirst-aws-nodejs

It will create 3 files for you
1-handler.js
2-gitignore
3-serverless.yml

serverless.yml -- Each service configuration is managed in the serverless.yml file

ex-:
service: aws-nodejs-serverless
provider:
name: aws
runtime: nodejs12.x
functions:
hello:
handler: handler.hello
events: - http:
path: /function1
method: get
function2:
handler: handler.function2
events: - http:
path: /function2
method: post

Setup your aws configuration with aws access key and secret key to deploy on
by following command

serverless config credentials — provider aws —key **_accesskey_** — secret **secretkey**

Finally deploy your code to aws by following command

serverless deploy

Each time add any code or function to project do this again - serverless deploy

