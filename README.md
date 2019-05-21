Node-RED Watson Bluemix Starter Application
======================================

## DEPRECATED: this repo is no longer actively maintained. It can still be used as reference, but may contain outdated or unpatched code. 

### Node-RED Watson in Bluemix

This repository is an example Node-RED application that can be deployed into
Bluemix with only a couple clicks. Try it out for yourself right now by clicking:

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/watson-developer-cloud/node-red-bluemix-starter.git)

**The `README.md` file *must* be updated, if you clone this repository, to point the *`Deploy to Bluemix` button* at your repository.**

This is a fork of the Node-RED in Bluemix boilerplate that integrates the following :

- All available Watson nodes for Node-RED on <a href="https://github.com/watson-developer-cloud/node-red-node-watson">GitHub</a>
- Flows from the <a href="https://github.com/watson-developer-cloud/node-red-labs/tree/master/basic_examples">Watson Node-RED Basics Labs</a>
- added Dropbox and Box nodes in the palette

Available Watson Nodes
This Boilerplate shows basics flows sample of the Watson nodes

- Alchemy Data News
- Alchemy Feature Extraction
- Conversation
- Discovery
- Document Conversion
- Language Identification
- Language Translation
- Natural Language Classifier
- Retrieve and Rank
- Speech to Text
- Text to Speech
- Tradeoff Analytics
- Tone Analyser
- Visual Recognition

### Notice
- this Watson Node-RED Boilerplate can be used as a starting point for demo or hackathon, but it is not intended for a production usage
- Watson nodes for Node-RED : these nodes are free of use, and are open-source under the Apache 2</p>
- Watson API / Bluemix services : those nodes needs to be linked with the appropriate Watson service in the Bluemix catalog, and support only one version of each the Watson API. The usage of those services are following a Cost Plan defined in the Bluemix catalog</p>

### How does this work?

When you click the button, you will be taken to Bluemix. The name of the application will be pre-filled *however* you can type your own name for your application, select the server and development space. Click the **DEPLOY button** and the application will be deployed with all samples and examples included in the Node-RED boilerplate.

It will automatically create an instance of the Cloudant service, call it `sample-node-red-cloudantNoSQLDB` and bind it to your app. This is where your Node-RED instance will store its data. If you deploy multiple instances of Node-RED from this repository, they will share the one Cloudant instance.

When you first access the application, you'll be asked to set some security options
to ensure your flow editor remains secure from unauthorised access.

It includes a set of default flows that are automatically deployed the first time
Node-RED runs.


### Customising Node-RED

This repository is here to be cloned, modified and re-used to allow anyone create their own Node-RED based application that can be quickly deployed to Bluemix.

The default flows are stored in the `defaults` directory in the file called `flow.json`.
When the application is first started, this flow is copied to the attached Cloudant
instance. When a change is deployed from the editor, the version in cloudant will
be updated - not this file.

The web content you get when you go to the application's URL is stored under the `public` directory.

Additional nodes can be added to the `package.json` file and all other Node-RED configuration settings can be set in `bluemix-settings.js`.

If you do clone this repository, make sure you update this `README.md` file to point the `Deploy to Bluemix` button at your repository.

If you want to change the name of the Cloudant instance that gets created, the memory allocated to the application or other deploy-time options, you will have to edit the `manifest.yml`.
