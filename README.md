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

## 

