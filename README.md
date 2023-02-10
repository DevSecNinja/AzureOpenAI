# Azure OpenAI

# Azure OpenAI API's in details connecting to other Azure and Microsoft Services

This GitHub repository serves as a  guide for users who want to establish a connection between different Azure services and Azure OpenAI. 

The repository provides step-by-step instructions, and other resources that will help users effectively and efficiently connect Azure services such as Azure Synapse, Microsoft Power Platform and others, to Azure OpenAI. 

Whether you are a beginner or an experienced developer, this repository will provide you with the information and tools you need to successfully connect Azure services to Azure Open AI.

Before to jumping to tye Azure OpenAI API, this guide will show how to have access to Azure OpenAI services in your Azure Subscription as well the step by step on how to setup this service.



## Topics that you will work in this guide:
* [Introduction of Using Open AI in Azure](https://github.com/hcmarque/AzureOpenAI/blob/main/README.md#introduction-of-using-open-ai-in-azure)
* [Enrolling Open AI in Azure](https://github.com/hcmarque/AzureOpenAI/blob/main/README.md#enrolling-in-openai-in-azure)
* [Creating an OpenAI instance in Azure after receving your confirmation]()
* [Exploring Azure OpenAI and Creating a deployment model](https://github.com/hcmarque/AzureOpenAI/blob/main/README.md#exploring-azure-openai-and-creating-a-deployment-model)
* [Exploring Azure OpenAI Studio and Summarization](https://github.com/hcmarque/AzureOpenAI/blob/main/README.md#exploring-azure-openai-studio-and-summarization)
* [Understanding the Max Length (tokens)](https://github.com/hcmarque/AzureOpenAI/blob/main/README.md#understanding-the-max-length-tokens)
* [Additional GPT-3 Playground models](https://github.com/hcmarque/AzureOpenAI/blob/main/README.md#additional-gpt-3-playground-models)



## Introduction of Using Open AI in Azure
Using OpenAI in Azure provides several advantages over using OpenAI standalone. Here are some of the key benefits of using OpenAI in Azure:

* **Integration with other Azure services**: By using OpenAI in Azure, you can easily integrate it with other Azure services such as Azure Machine Learning, Azure Databricks, and others, which can help you streamline your workflows and achieve your goals faster.

* **Scalability**: Azure provides a scalable platform that can help you meet the demands of your applications and workloads, regardless of the size of your deployment. This can be particularly beneficial for organizations that need to process large amounts of data or run computationally intensive workloads.

* **Reliability and security**: Azure is a highly secure and reliable platform that provides a number of features and tools to help you protect your data and applications. By using OpenAI in Azure, you can benefit from the security and reliability of the Azure platform.

* **Cost-effectiveness**: Azure provides a cost-effective solution for running and managing applications and workloads. This can be particularly important for organizations with limited budgets that need to get the most out of their resources.

* **Access to expert support**: By using OpenAI in Azure, you can benefit from the support of a highly skilled and experienced team of experts who can help you with any questions or issues you may have.

In summary, using OpenAI in Azure provides a more integrated, scalable, secure, cost-effective, and supported solution for organizations looking to leverage the power of OpenAI


## Enrolling in OpenAI in Azure

The fisrt step here would be to enroll to joining the Managed Azure Open AI General Availability in your subscription. 
Use this link ASAP Submit this form to apply for access. Engineering will work to approve your access in 3-10 business days.

[link](https://customervoice.microsoft.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR7en2Ais5pxKtso_Pz4b1_xUOFA5Qk1UWDRBMjg0WFhPMkIzTzhKQ1dWNyQlQCN0PWcu)

![image](https://user-images.githubusercontent.com/13455341/218121565-daacf1b8-64cb-4618-928d-98ebb4a6c4de.png)


## Creating an Azure OpenAI instance after receving your confirmation

* In your [Azure Portal](https://ms.portal.azure.com/), proceed with the login using your user that has the subscription ID used on the last step to register on OpenAI.

* On the search bar, type Azure OpenAI

![Recording 2023-02-10 at 09 19 09](https://user-images.githubusercontent.com/13455341/218114411-3ab50339-9f76-4e6a-9596-93713886b0f7.gif)


* As soon as you have your Azure OpenAI created, please create an instance of Azure OpenAI clicking on Create

* On Create Azure OpenAI:
- Select the Subscription
- Resorce Group: Create new OR use any another already created, in this case, a OpenAI Resorce Group was created.
- Region: In this exemple, a Esat US was selected, there are other 2 options: South Central US or West Europe. Feel free to pickup the one that is aligned with your region.
- Provide a name for the Instance, in this example, the OpenAI-Github was used.
- Pricing Tier: Standard S0
- Click in Review + Create and create your instance

![Recording 2023-02-10 at 09 21 21](https://user-images.githubusercontent.com/13455341/218114836-c98d89d9-0923-47c9-9856-da479322aca4.gif)


Click in Go to Resource

![image](https://user-images.githubusercontent.com/13455341/218115794-9a8f7be8-6618-4979-b395-cac2f4283c2c.png)


## Exploring Azure OpenAI and Creating a deployment model

Entering on the Azure OpenAI Instance, click on "Explore"

![image](https://user-images.githubusercontent.com/13455341/218116217-81b08e85-0dcf-4d2c-841c-a614dae19272.png)


Once there, you will be able to find the ways to get started with Azure OpenAI Service and explore examples for promprt completion. 

As a next step, click in "Create new deployment"

![Recording 2023-02-10 at 09 36 04](https://user-images.githubusercontent.com/13455341/218118277-d01d7d1b-ec3f-437a-be52-4ca2671d1887.gif)

On the Deploy Model, you should chose for Model name. There are few options, Davinci is the most capable model family and can perform any task the other models can perform and often with less instruction. 

For applications requiring a lot of understanding of the content, like summarization for a specific audience and creative content generation, Davinci is going to produce the best results. You can have more details about other models checking [here](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/concepts/models#davinci)

Just a observation: No worries, build your Model using Davinci text 3 and the Azure Open AI Playground will let you know which model you should be using for which specific use case ;-)

![Recording 2023-02-10 at 09 44 48](https://user-images.githubusercontent.com/13455341/218120265-d776288c-93dc-4ef2-a917-40fb4f3ba407.gif)

## Exploring Azure OpenAI Studio and Summarization

As soon as you have your model created, click on the Deployed Model
And them, click in "Open in Playground"

![Recording 2023-02-10 at 09 46 07](https://user-images.githubusercontent.com/13455341/218120434-ee36aea5-228d-4cb0-9122-d13aceb043b5.gif)

Now it's time to work on the Model that you just deployed on the previous step. Select the Deployment Model, in this example, "text-davinci-003" and as well one of the examples or use cases that you are targeting, in this example, "Summarize Text" will be used.

![Recording 2023-02-10 at 09 47 37](https://user-images.githubusercontent.com/13455341/218120850-585fb31c-ae8c-4b85-9c7a-693e39fcf427.gif)

You will be able to see that a message will appers showing which Model this example would works better. In case of Summarization, the model text-davinci-002 would works better. Click on "Create deployment"

As a new Deployment model was created, named "text-davinci-002", select it, as well the "Summarize text" and click in Generate on the botton of the page to see the results of the example, in green.

![Recording 2023-02-10 at 09 49 12](https://user-images.githubusercontent.com/13455341/218121184-b98b0730-a294-4eec-8be5-4af8b3fe580c.gif)

## Understanding the Max Length (tokens)

The Max lenght (tokens) on Azure OpenAI means a set a limit on the number of tokens to generate in a response. The system supports a maximum of 4000 tokens shared between a given prompt and response completion. (One token is roughly 4 characters for typical English text.)

Token refers to a unit of text used to represent a word or piece of punctuation in a computational process. Tokens are often used as the basis for processing and generating natural language text using artificial intelligence models such as OpenAI's GPT-3. The number of tokens in a given piece of text can impact the complexity of processing and generating a response, and setting a token limit can help to ensure that the generated response remains concise and manageable.

## Additional GPT-3 Playground models

Azure OpenAI Studio is a platform that provides access to OpenAI's advanced AI technologies, including its cutting-edge language models, to help businesses and developers build advanced applications. Some of the services available in Azure OpenAI Studio include:

* GPT-3 Language Model: This is the latest and most advanced language model from OpenAI, capable of performing a wide range of natural language processing tasks such as text generation, language translation, and sentiment analysis.

* Text Generation: A service that allows you to generate new text based on a prompt or sample text, using the GPT-3 language model.

* Text Classification: A service that allows you to classify text into predefined categories based on its content, using machine learning algorithms.

* Named Entity Recognition: A service that identifies named entities in text, such as people, organizations, and locations.

* Sentiment Analysis: A service that analyzes the sentiment or emotional tone of a piece of text.

* Text Translation: A service that translates text from one language to another.

* Natural Language to SQL:  This service can be used to simplify the process of querying databases, as it enables users to ask questions in plain English and receive results in the form of structured data.


![Recording 2023-02-10 at 11 57 37](https://user-images.githubusercontent.com/13455341/218150823-b92b6633-69a8-4284-95d0-5ae391b2ee90.gif)

These are just a few examples of the services available in Azure OpenAI Studio. The platform is continually evolving and expanding its capabilities, so new services and features may become available in the future. 









