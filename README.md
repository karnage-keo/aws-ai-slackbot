# Creating an AWS AI Chatbot
## Project: DilBot
![Screenshot 2024-10-11 at 07 05 03](https://github.com/user-attachments/assets/3bd2dec4-9094-4602-b369-1f55b80489f4)

## Introduction

This document details the development and implementation of DilBot, an AI-powered chatbot designed to integrate with Slack. This project served as a practical application of various Amazon Web Services (AWS) AI and search technologies, showing their capabilities in creating intelligent, conversational interfaces from organisational data . The primary goal was to build a robust chatbot that could not only engage in natural language conversations but also retrieve specific, domain-based information from diverse enterprise data sources (RAG).

## Projet Goals and Objectives

The core objectives for the DilBot project were:

- To leverage AWS services, particularly in the realm of Artificial Intelligence, to build a functional chatbot.
- To enable the chatbot to understand natural language queries and provide relevant responses.
- To integrate the chatbot with Slack, making it easily accessible to users within their existing communication platform.
- To allow the bot to access information from sources, and use them to assit users.
- A bonus goal included exploring potential integration with Amazon Alexa or Google Assistant for voice-based interactions.

## Technologies used

The DilBot project primarily utilised the following key AWS services and third-party integrations:

__Amazon Lex:__ This service was the cornerstone for building the conversational interface of the chatbot. Amazon Lex allowed for the design of natural language understanding (NLU) capabilities, enabling the bot to interpret user intents and extract relevant information from their requests. Lex handles the conversations with the end users, and assists in providing the criteria required when searching for data. 

__Amazon Kendra:__ To provide the bot with the ability to answer questions based on specific organizational data (RAG), Amazon Kendra was employed. Kendra is an intelligent enterprise search service that uses machine learning to index and search across various data repositories. For DilBot, this included the potential to connect to sources like Jira, Confluence, and Google Drive, allowing the bot to retrieve information from these diverse platforms.

__Slack:__ The chosen platform for the chatbot's deployment and user interaction was Slack. This integration allowed users to interact with DilBot directly within their Slack channels, leveraging Slack's familiar interface for commands and responses.

__Amazon Q (Considered Alternative):__ While Amazon Lex and Kendra formed the core, Amazon Q was considered as a potential alternative, highlighting the exploration of different managed chatbot solutions offered by AWS. Amazon Q offers a more integrated, subscription-based approach to building generative AI applications. The main detractor from Amazon Q was the ongoing cost management for a subscription based service.

## Architecture and Integration

The architecture of DilBot is designed to facilitate a fluid interaction between the user, the Slack platform, and the AWS backend services.

User Interaction via Slack: Users initiate conversations with DilBot directly within a Slack channel. Their messages are sent to the Slack API.

Slack Integration with Amazon Lex: Slack is configured to forward incoming messages to an Amazon Lex bot. This typically involves setting up an API Gateway endpoint or a Lambda function that acts as a bridge, receiving messages from Slack and passing them to Lex.

Amazon Lex as the Conversational Core: Amazon Lex processes the user's input. It identifies the user's intent (e.g., "ask a question," "get information about X") and extracts any necessary slots (e.g., the specific topic of the question).

Intent Fulfilment with Amazon Kendra: For intents requiring data retrieval, Amazon Lex is configured to invoke an AWS Lambda function. This Lambda function then acts as an intermediary, taking the extracted intent and slots and formulating a query for Amazon Kendra.

Amazon Kendra for Intelligent Search: Kendra performs an intelligent search across its indexed data sources (e.g., Jira, Confluence, Google Drive). It retrieves the most relevant documents or snippets that answer the user's query.

Response Generation and Delivery: The results from Amazon Kendra are sent back to the Lambda function, which then formats the answer. This formatted response is then passed back to Amazon Lex. Lex, in turn, sends the final response back to Slack, where it is displayed to the user.

Generative AI Capabilities: Beyond direct data retrieval, the integration of generative AI (likely through Lex's capabilities or a connected LLM via Lambda) allows DilBot to engage in more free-form discussions and provide more human-like responses when direct answers aren't found or for general conversational purposes.

This architecture ensures that DilBot can handle both structured queries requiring specific data lookup and more open-ended conversational interactions, providing a comprehensive AI assistant experience within Slack.

## Configuring Amazon Kendra

## Configuring Amazon Lex

## Configuring Slack API integration

## Bot testing & Adjustments

## Configuring Alexa Dilbot

## Conclusion







