# NodeJS GCM Challenge
A NodeJS challenge for sending data to android devices via Google Cloud Messaging

## Introduction

In this challenge you are going to write a simple nodejs library named `node-gcm-xmpp` which sends [downstream](https://developers.google.com/cloud-messaging/downstream) XMPP messages over socket.
It is supposed to be a simple library sending messages via XMPP over socket, right now we don't care about advanced options such as delay_while_idle, delivery, queue management, etc.

We should be able to use your library this way:

    var gcm = require('node-gcm-xmpp');

    var message = new gcm.Message();

    message.addData('key1', 'msg1');

    var regTokens = ['YOUR_REG_TOKEN_HERE'];

    // Set up the sender with you API key
    var sender = new gcm.Sender('YOUR_API_KEY_HERE');

    // Now the sender can be used to send messages
    sender.send(message, { registrationTokens: regTokens }, function (err, response) {
      if(err) console.error(err);
      else    console.log(response);
    });

This challenge can be done within a few days depending on the developer's experience.

## Expectations

### Estimation

After reading and understanding the challenge and all of expectations, estimate the challenge development cost, send us your time cost estimation and your reasoning on how you've estimated this. **Do not start development before getting a confirmation from us**.

### Private Repo

Create a private git repositry named `node-gcm-xmpp` and share it with us. you can use [bitbucket](https://bitbucket.org/product/pricing) for free. Just do it, there are some points in making it private.

### Gitflow

Apply gitflow to your repository and follow its guidelines during your development. You are supposed to release version 0.1.0 at the end of this challange.

### README

Include a readme file describing how to install, test and use your library.

### Tests

Create unit tests with the testing framework of your choice. A good test coverage is expected.

### CI

Integrate your repository with [shippable](https://app.shippable.com/pricing.html). Don't worry! Configuration is almost the same as [Travis-CI](https://travis-ci.org/), considering you've already worked with latter one.

### Code Quality

Integrate your project with [codacy](http://codacy.com/). We do like to see your code quality, coverage and branch report. You'll need to setup code analysis and coverage report at codacy.


