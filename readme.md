# Azure DevOps Pipeline Template for Node.js Applications

This Azure DevOps pipeline template is designed to help you set up a continuous integration and deployment pipeline for your Node.js applications. It includes build and deploy stages, allowing you to build your application and deploy it to Azure Web App on Linux.

## Prerequisites

Before using this template, ensure you have the following:

- An Azure DevOps account.
- An Azure subscription and Resource Group etc.
- An Azure web app
- A Node.js application with a valid `package.json` file.

## Usage

1. Copy the content of `azure-pipelines.yml` into the `azure-pipelines.yml` file in the root of your Azure DevOps repository.

2. Customize the variables in the `azure-pipelines.yml` file based on your project requirements:

   - `azureSubscription`: Your Azure subscription name.
   - `appName`: Name of your Azure Web App.
   - `resourceGroupName`: Name of your Azure Resource Group.
   - `location`: Azure region where your resources will be deployed.
   - `nodeVersion`: Node.js version to be used in the build.

3. Commit and push the changes to trigger the Azure DevOps pipeline.

## Pipeline Structure

- **Build Stage:**
  - Installs Node.js.
  - Builds the Node.js application.
  - Publishes the build artifacts.

- **Deploy Stage:**
  - Deploys the application to Azure Web App on Linux.
  - Uses a custom deployment script to install production dependencies.
