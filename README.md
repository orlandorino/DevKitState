---
title: "DevKit State"
permalink: /docs/projects/devkit-state/
excerpt: "You can use this example to monitor MXChip IoT DevKit states and control the user LED with Azure IoT Hub device twins, including WiFi information and sensor states."
header:
  overlay_image: /assets/images/projects-iothub.jpg
  overlay_full: true
  teaser: /assets/images/projects-iothub-th.jpg
icons:
  - url: /assets/images/icon-iot-hub.svg
    target: https://azure.microsoft.com/en-us/services/iot-hub/
    title: IoT Hub
difficulty: EASY
last_modified_at: 2017-10-18
---

{% include toc icon="columns" %}

You can use this example to monitor MXChip IoT DevKit states and control the user LED with Azure IoT Hub device twins, including WiFi information and sensor states.

## Steps to start

1. Setup development environment by following [Get Started](https://microsoft.github.io/azure-iot-developer-kit/docs/get-started/)
2. `git clone https://github.com/DevKitExamples/DevKitState.git`
3. `cd DevKitState`
4. `code .`

## Provision Azure Services

1. Click **Task** menu in Visual Studio Code - **Run Task...** - **cloud-provision**
2. Select a subscription
3. Select or choose a resource group (if you have already had a free IoT Hub, this step will be skipped)
4. Select or create an IoT Hub
5. You will see something like *function app: function app name: xxx*, write down the function app name, and we will use it in later step
6. Wait for ARM template deployment

## Deploy Function App

1. Click **Task** menu in Visual Studio Code - **Run Task...** - **cloud-deploy**
2. Wait for function app code uploading

## Configure IoT Hub Device Connection String in DevKit

1. Connect your DevKit to your machine
2. Click **Task** menu in Visual Studio Code - **Run Task...** - **config-device-connection**
3. Hold button A on DevKit, then press rest button, and then release button A to enter config mode
4. Wait for connection string configuration

## Uploade Arduino Code to DevKit

1. Connect your DevKit to your machine
2. Click **Task** menu in Visual Studio Code - **Run Build Task...**
3. Wait for arduino code uploading

## Monitor DevKit State in Browser

1. Open `DevKitState\web\index.html` in browser
2. Input the function app name you write down
3. Click connect button
4. You should see DevKit state in few seconds

## Control DevKit User LED

1. Click User LED on the web page
2. You should see user LED state changed in few seconds

## Screenshots

![](https://raw.githubusercontent.com/DevKitExamples/DevKitState/master/screenshots/devkit-state.png)

## License

MIT License

Copyright (c) Microsoft Corporation. All rights reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

{% include feedback.html tutorial="happy-path" %}