---
permalink: /siren-ai/changelog
---
# Siren AI changelog

## 1.3.0

- K9 chat and report generation prompts can now be customized in the advanced settings ⚙️
- Graph serialization has been turbo-charged, so now graphs up to three times larger can be sent to the LLM 🦣
- Minor doc improvements 📑
- Fixed issue where references to EIDs in the graph aren't clickable 🖱️
- Fixed issue where EIDs couldn't be styled by K9 Chat Companion

## 1.2.0

- K9 improvements
    - References to documents in K9's messages are now clickable and will open in the record viewer 🔗
    - Support for styling edges in the graph ✨
    - Support for local nodes in graphs ⭕
    - Emoticons are no longer converted to emojis :)
- Minor UI improvements
- Improved error messages
    - When graph is too large
    - When generated graph report can not be downloaded
- Documentation fixes
    - Fixed some scripting examples

## 1.1.0

- K9 Companion now available!
    - Chat with the LLM from the Investigate UI 💬
    - Graph-aware: You can ask questions about the graph you're looking at 🕸️
    - K9 can set node styles in response to your questions 💅
- Improvements to generated graph report
    - Added an image of the graph to downloaded reports
    - Report title now uses the name of the graph
    - "Introduction" section removed
    - Renamed "Graph Nodes" section to "Selected Nodes"
- Scripting API improvements:
    - Support for a custom LLM prompt when generating a report
    - Added autocompletion for Siren AI methods in the Investigate script editor
- Other minor UX improvements
- Improved error messaging
    - When Siren AI plugin is disabled
    - When graph is too big
- Documentation fixes:
    - Updated config option "ollama.connectin.endpoint" to "ollama.connection.host"

## 1.0.1

- Fix crash when using Investigate with security disabled

## 1.0.0

- Generate downoadable reports using AI from the graph browser 📄
- Siren scripting API methods for sending messages and generating reports
- Support for OpenAI, Azure OpenAI, Ollama and AWS Bedrock
- Permissions for configuraing access to Siren AI features
- Support for auditing LLM queries
