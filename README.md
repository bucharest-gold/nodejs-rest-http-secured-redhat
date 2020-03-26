[![Build Status](https://travis-ci.org/nodeshift-starters/nodejs-rest-http-secured-redhat.svg?branch=master)](https://travis-ci.org/nodeshift-starters/nodejs-rest-http-secured-redhat) [![Coverage Status](https://coveralls.io/repos/github/nodeshift-starters/nodejs-rest-http-secured-redhat/badge.svg?branch=master)](https://coveralls.io/github/nodeshift-starters/nodejs-rest-http-secured-redhat?branch=master) [![Greenkeeper badge](https://badges.greenkeeper.io/nodeshift-starters/nodejs-rest-http-secured-redhat.svg)](https://greenkeeper.io/)

https://access.redhat.com/documentation/en-us/red_hat_build_of_node.js/

# nodejs-rest-http-secured-redhat
Quickstart to expose a REST Greeting endpoint using Node.js&amp; Secured by Red Hat SSO


## SSO Server Setup

This application requires a Red Hat SSO Server to be running.  You can create one easily by using the `service.sso.yaml` file by running:

    oc create -f service.sso.yaml


## deploying the Application

You will need to know the Auth URL from the SSO server that was deployed in the previous step.

To deploy the application, run:

    npm run openshift -- -d SSO_AUTH_SERVER_URL=<auth url from sso server>
