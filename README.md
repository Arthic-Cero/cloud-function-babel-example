# cloud-function-babel-example
Google Cloud Functions Hello World example with Babel and Bunyan logging library.

## Prerequisites
1. [Google Cloud SDK](https://cloud.google.com/sdk/)
2. [node and npm](https://www.npmjs.com/get-npm) 

## Function Code
See file [index.es7](index.es7) for the Hello World function code. It uses some syntax that is not supported natively by Cloud Functions (import). The code will be transpilled to the supported node runtime (v6.11.5) in Cloud functions using [BabelJS](https://babeljs.io/) CLI.

See the [functions/package.json](functions/package.json) file for the `prepare` script which runs the transpilation step.

## Deploy
1. Clone or download this repo and open the `cloud-function-babel-example`
2. Install the dependencies locally by running `npm install`
3. Transpile the code by running `npm run prepare`
4. Deploy to your GCP project by runnning `gcloud beta functions deploy helloWorldFun --trigger-http`
