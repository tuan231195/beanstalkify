[AWS Elastic Beanstalk](http://aws.amazon.com/elasticbeanstalk/) automation. A work in progress.
This is the node version of [Ruby Beanstalkify](https://github.com/pranavraja/beanstalkify/) 

[![Build Status](https://travis-ci.org/liamqma/beanstalkify.svg?branch=master)](https://travis-ci.org/liamqma/beanstalkify)
[![Coverage Status](https://coveralls.io/repos/liamqma/beanstalkify/badge.svg?branch=master&service=github)](https://coveralls.io/github/liamqma/beanstalkify?branch=master)

## Install
```bash
    npm install beanstalkify --save
```

## Usage

```javascript
var Application = require('beanstalk');
var application = new Application(
    {
        accessKeyId: 'XXX',
        secretAccessKey: 'XXX',
        region: 'ap-southeast-2'
    }
);

application.deploy(
{
    archiveFilePath: 'PATH TO ZIP FILE',
    environmentName: 'CNAME',
    awsStackName: '64bit Amazon Linux 2015.03 v2.0.0 running Node.js',
    beanstalkConfig: [
        Beanstalk options
        ....
    ],
    outputFile: 'OUTPUT JSON FILE'
}
);
```

## Test

```bash
npm test
```