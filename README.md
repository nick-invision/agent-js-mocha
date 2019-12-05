### Mocha reporter for EPAM report portal [clone of https://github.com/fedoseev-vitaliy/mocha-rp-reporter]
This is mocha runtime reporter for [EPAM report portal](https://github.com/reportportal/reportportal).

It was designed to work with mocha programmatically, in order to be able to parametrize each test run.


#### Installation steps:

` npm install rp-mocha-reporter`

#### How to use:
Fill in reporterOptions. 
```javascript
const Mocha = require("mocha");
let mochaMain = new Mocha({
    reporter: 'mocha-rp-reporter',
    reporterOptions: {
        endpoint: "",
        token: "",
        launch: "",
        project: "",
        tags: [] // optional string array of tags
    }
});
```

#### Run test example:
For running test example clone [agent-js-mocha](https://github.com/reportportal/agent-js-mocha) and fill in [reporterOptions](#How-to-use).  

In the working directory run:  
1. ```npm install```  - that would install all dependencies.

2. ```npm test``` - that would run example tests.