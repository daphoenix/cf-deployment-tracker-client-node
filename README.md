# Overview

This is an npm module that can track and report details of a demo/tutorial that has been deployed to Cloud Foundry.

# To Use

1. Open a terminal and run  
   ```
   npm install cf-deployment-tracker-client --save
   ```
2. Require the package in your main entry point to your app (probably app.js).  
    ```
    require("cf-deployment-tracker-client").track();
    ```
3. Add a copy of the Privacy Notice to the readme file. 

   **Note:** All apps that have deployment tracker must include the Privacy Notice.

# Example app

To see how to include this into your app please visit [Bluemix Hello World](https://github.com/IBM-Bluemix/bluemix-hello-node).  You will want to pay attention to [package.json](https://github.com/IBM-Bluemix/bluemix-hello-node/blob/master/package.json#L9), and [server.js](https://github.com/IBM-Bluemix/bluemix-hello-node/blob/master/server.js#L15).

# Privacy Notice

Sample web applications that include this package may be configured to track deployments to [IBM Bluemix](https://www.bluemix.net/) and other Cloud Foundry platforms. The following information is sent to a [Deployment Tracker](https://github.com/IBM-Bluemix/cf-deployment-tracker-service) service on each deployment:

* Node.js package version
* Node.js repository URL
* Application Name (`application_name`)
* Space ID (`space_id`)
* Application Version (`application_version`)
* Application URIs (`application_uris`)
* Labels of bound services
* Number of instances for each bound service and associated plan information

This data is collected from the `package.json` file in the sample application and the `VCAP_APPLICATION` and `VCAP_SERVICES` environment variables in IBM Bluemix and other Cloud Foundry platforms. This data is used by IBM to track metrics around deployments of sample applications to IBM Bluemix to measure the usefulness of our examples, so that we can continuously improve the content we offer to you. Only deployments of sample applications that include code to ping the Deployment Tracker service will be tracked.

## Disabling Deployment Tracking

Please see the README for the sample application that includes this package for instructions on disabling deployment tracking, as the instructions may vary based on the sample application in which this package is included.
