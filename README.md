[![Build Status](https://travis-ci.org/bucharest-gold/nodejs-rest-http-secured-redhat.svg?branch=master)](https://travis-ci.org/bucharest-gold/nodejs-rest-http-secured-redhat) [![Coverage Status](https://coveralls.io/repos/github/bucharest-gold/nodejs-rest-http-secured-redhat/badge.svg?branch=master)](https://coveralls.io/github/bucharest-gold/nodejs-rest-http-secured-redhat?branch=master) [![Greenkeeper badge](https://badges.greenkeeper.io/bucharest-gold/nodejs-rest-http-secured-redhat.svg)](https://greenkeeper.io/)

# nodejs-rest-http-secured-redhat
Quickstart to expose a REST Greeting endpoint using Node.js&amp; Secured by Red Hat SSO


## SSO Server Setup

This booster requires a Red Hat SSO Server to be running.  You can create one easily by using the `service.sso.yaml` file by running:

    oc create -f service.sso.yaml


## deploying the Booster

You will need to know the Auth URL from the SSO server that was deployed in the previous step.

To deploy the booster, run:

    npm run openshift -- -d SSO_AUTH_SERVER_URL=<auth url from sso server>
