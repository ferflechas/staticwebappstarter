# Document Processing Accelerator

## React basic

[Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview) allows you to easily build [React](https://reactjs.org/) apps in minutes. Use this repo with the [React quickstart](https://docs.microsoft.com/azure/static-web-apps/getting-started?tabs=react) to build and customize a new static site.

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Overview
The goal of this repository is to build a comprehensive set of tools and examples

<Insert screenshot of output here>

![](https://github.com/brandoncwn/staticwebappstarter/blob/main/Sample_Architecture1.png)

## Algorithms
### Text Classification
Text classification is a supervised learning method of learning and predicting the category or the class of a document given its text content. The state-of-the-art methods are based on neural networks of different architectures as well as pre-trained language models or word embeddings.
### Custom Named Entity Recognition
Named Entity Recognition (NER) is the task of detecting and classifying real-world objects mentioned in text. Common named entities include person names, locations, organizations, etc. The state-of-the art NER methods include combining Long Short-Term Memory neural network with Conditional Random Field (LSTM-CRF) and pretrained language models like BERT.

NER usually involves assigning an entity label to each word in a sentence as shown in the figure below.

 Fine-tuned BERT for NER tasks

O: Not an entity  
I-LOC: Location  
I-ORG: Organization  
I-PER: Person  

There are a few standard labeling schemes and you can find the details [here](http://cs229.stanford.edu/proj2005/KrishnanGanapathy-NamedEntityRecognition.pdf). The data can also be labeled with custom entities as required by the use case.
## Target Audience
For this repository our target audience includes data scientists and machine learning engineers with varying levels of NLP knowledge as our content is source-only and targets custom machine learning modelling. The utilities and examples provided are intended to be solution accelerators for real-world NLP problems.

## Prerequisities
1. Github account
2. Resource group access
    a. Select preferred region
3. Ensure that you have accepted terms and conditions for Responsible AI
 "You must create your first Face, Language service, or Computer Vision resources from the Azure portal to review and acknowledge the terms and conditions. You can do so here: Face, Language service, Computer Vision. After that, you can create subsequent resources using any deployment tool (SDK, CLI, or ARM template, etc) under the same Azure subscription."

## Installation Steps
### 1. Clone repo https://github.com/jameshoff-msft/bpa-backend
### 2. Create a Resource Group in your Azure Portal
### 3. Import Git Repo
### 4. Setting up Azure DevOps Pipeline
You'll use Azure DevOps for running the multi-stage pipeline with build. If you don't already have an Azure DevOps organization, create one by following the instructions at [Quickstart: Create an organization or project collection.](If you don't already have an Azure DevOps organization, create one by following the instructions at Quickstart: Create an organization or project collection.)
###     1. Navigate to Azure DevOps www.dev.azure.com
###     1. Select Repos
###     1. Select Import a Repository https://github.com/jameshoff-msft/bpa-backend
 Cloning may take several minutes. Your cloned repository should mirror the below directory:
 ![](https://github.com/brandoncwn/staticwebappstarter/blob/main/cloned_repository.png)
###     1. Project settings (bottom left)
###     1. Create Service Connection - 3rd one azure resource manager. Select 'grant access to all pipelines'
 * note alphanumeric lower case only as multiple azure services and resources are being used with different naming convention restrictions
 * 
###     1. Create pipeline
###     2. update lines 12-17
 ---azure subscription = service connection previously created
 ---project name has to be unique
 ---fill in resource group
 ---fork 'static' - which is the front end repo - to your own repo
 ------copy url <> 
 ---go to settings / developer settings / go to personal access token, select "workflow" level, create token name. Copy and save this token somewhere for future use (if lost a new token will need to be geenreated
### click save and run. insert any commit message
 You should see the pipeline stages workflow updating

6. Create Service Connection




## Roadmap

## References
https://github.com/microsoft/nlp-recipes/tree/master/examples/named_entity_recognition
https://github.com/microsoft/nlp-recipes/tree/master/examples/text_classification
