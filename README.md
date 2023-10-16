# Welcome to your CDK TypeScript project

This is a blank project for CDK development with TypeScript.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `cdk deploy`      deploy this stack to your default AWS account/region
* `cdk diff`        compare deployed stack with current state
* `cdk synth`       emits the synthesized CloudFormation template

Index creation:
--------------
curl -u master_username:master_password -X PUT "<ES_URL>/<ES_INDEX>?pretty"
Indexing Single Doc:
-------------------
curl -XPUT -u 'master_username:master_password' '<ES_URL>/<ES_INDEX>/_doc/1' -d '{"director": "Burton, Tim", "genre": ["Comedy","Sci-Fi"], "year": 1996, "actor": ["Jack Nicholson","Pierce Brosnan","Sarah Jessica Parker"], "title": "Mars Attacks!"}' -H 'Content-Type: application/json'
Bulk Loading of Data:
---------------------
curl -XPUT -u 'master_username:master_password' '<ES_URL>/<ES_INDEX>/_bulk?pretty' --data-binary @/path/to/json/data/file/<file-name>.json -H 'Content-Type: application/json'
Search Index:
-------------
curl -XGET -u 'master_username:master_password' '<ES_URL>/<ES_INDEX>/_search?q=rebel&pretty=true'

here are the commands we've used the

