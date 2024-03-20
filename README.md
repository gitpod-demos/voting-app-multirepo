<img src="https://www.gitpod.io/images/media-kit/logo-dark-theme.png" width="250">

# Always ready-to-code 🍊
Gitpod is the developer platform for on-demand Cloud Development Environments (CDEs). Say goodbye to slow onboarding and unmanageable dev environments. Gitpod removes pain and frustration from your developer experience, helps you deliver software faster, and makes you more secure and compliant.

## Why Gitpod?
Here are some of the reasons devops, security, and finance teams love Gitpod:

👩🏻‍💻 Faster developer onboarding  
⚙️ Eliminate software dependency issues  
🤝 Collaborate async or in real time  
☁️ Utilize the compute power of the cloud  
💰 Save money on hardware and virtual infrastructure  
🔐 Secure and protect your code and dev environments

## About this Demo Example
This multi-repo demo example contains a simple voting application that can be launched in Docker compose. The `Vote`, `Worker` and `Result` components live on separate repositories but they are all brought into and built inside a single Gitpod dev environment (please see diagram and architecture below).
You can try it yourself right now! Simply click the link below to launch a new Gitpod workspace where you can play with the voting application in any web browser. No extra software is required, all you need is a free Gitpod account:

https://gitpod.io/#https://github.com/gitpod-demos/voting-app-multirepo

## Architecture

<img src="/architecture.excalidraw.png" width="500">

* A front-end web app in [Python](/vote) which lets you vote between two options (hosted [here](https://github.com/gitpod-demos/voting-app-vote))
* A [Redis](https://hub.docker.com/_/redis/) which collects new votes
* A [.NET](/worker/) worker which consumes votes and stores them in Postgres (see below) (hosted [here](https://github.com/gitpod-demos/voting-app-worker))
* A [Postgres](https://hub.docker.com/_/postgres/) database backed by a Docker volume
* A [Node.js](/result) web app which shows the results of the voting in real time (hosted [here](https://github.com/gitpod-demos/voting-app-result))

You can also use the [Gitpod browser extension](https://chrome.google.com/webstore/detail/gitpod-always-ready-to-co/dodmmooeoklaejobgleioelladacbeki) to launch a workspace from *any* Github repo of your choice!


