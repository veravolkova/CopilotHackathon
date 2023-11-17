# GitHub Copilot Hackaton using Nodejs, .NET and Java 

- [Goal](#goal)
- [Pre-requisites](#pre-requisites)
- [Work with Github Codespaces](#work-with-github-codespaces)
- [Work locally](#work-locally)
- [Instructions](#instructions)

## Goal

The goal of this exercise is to learn how to use GitHub Copilot for building a .NET Web API or Node.js and Java Rest API (either Spring Boot or Quarkus).

GitHub Copilot is an AI-powered code assistant that helps developers write better code faster. It uses machine learning models trained on billions of lines of code to suggest whole lines or entire functions based on the context of what you’re working on. By using Copilot, you can learn how to write better code and improve your productivity.

Remember:

- As you type GitHub Copilot will make suggestions, you can accept them by pressing Tab.
- If nothing shows up after Copilot write some lines , press enter and wait a couple of seconds.
- On Windows, MacOS or Linux, press Ctrl + Enter, then click Open GitHub Copilot.
- Alternatively you can use right-click menu to start Copilot inline chat or open a chat window by clicking a chat icon on a left side panel.

## Pre-requisites

**GitHub Codespaces access**

Make sure your Codespaces monthly usage quota has not been exceeded [Viewing your GitHub Codespaces usage]( https://docs.github.com/en/billing/managing-billing-for-github-codespaces/viewing-your-github-codespaces-usage). 

Once reached the free limit, you can complete the exercises locally in VS Code using Copilot extension [GitHub Copilot in VS Code](https://code.visualstudio.com/docs/editor/github-copilot).
Please see [Work locally](#work-locally) for further guidance.

## Work with GitHub Codespaces

Environment is already configured to work with Github Codespaces, you can find the configuration files in the .devcontainer folder.

To start programming just start a new codespace and you are ready to go, don't need to install anything.

1. In a browser, go to https://github.com/GitHub-Accenture-Finland/CopilotHackathon.

2. Click on the `<> Code` button, and then the `Codespaces` tab.

3. Click the plus sign icon (+) to create a codespace with default settings. Please note that it may take a while to load it for the first time.

You can choose to click the ellipses (...) at the top of this window and choose `+ New with options...` to create a codespace with more cores to speed up things.
However, a more powerful codespace will take more usage quota.

### Work locally

**VisualStudio Code**

https://code.visualstudio.com/

**Install Docker**

https://docs.docker.com/engine/install/

**For Nodejs**

- [Install Node and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- Install mocha: 

Run:

``` bash
 npm install --global mocha
 npm install axios
```

**For .NET**

[Install .Net](https://dotnet.microsoft.com/download)

**For Java**

- [Install Java](https://learn.microsoft.com/en-us/java/openjdk/install)
- [Install Maven](https://maven.apache.org/install.html)


## Instructions

- [Node Server](./exercisefiles/node/README.md)
- [.NET Web API](./exercisefiles/dotnet/README.md)
- [Java Spring Boot](./exercisefiles/springboot/README.md)
- [Java Quarkus](./exercisefiles/quarkus/README.md)
