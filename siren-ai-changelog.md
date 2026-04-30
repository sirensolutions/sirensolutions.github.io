---
permalink: /siren-ai/changelog
---
# Siren AI changelog

## 2.0.0

- Breaking changes
  - The siren-ai configuration format has changed to support multiple models. Please refer to the [documentation](https://docs.siren.io/siren-ai/2.0/siren-ai/t_configuring.html) for the updated configuration format

- New features
  - K9 now supports multiple languages with full i18n support, enabling global usage
  - Added tool support for AWS Bedrock enabling K9 to perform actions when using AWS-hosted models
  - Ollama now uses a generic OpenAI-compatible provider config instead of Ollama-specific one, improving compatibility and flexibility
  - Users can now select from multiple configured AI models at runtime
  - Edge references now render as interactive badges with visual styling, improving graph readability
  - Added keyboard shortcuts to quickly open and close K9 interface without using mouse
  - Added visible close button for K9 popover instead of relying only on clicking outside
  - K9 now has awareness of and can reference combo/group nodes in graphs, enhancing support for complex graph structures

- Improvements
  - K9 global search tool now supports non-range date queries, providing more flexible filtering options
  - AI provider errors are now displayed directly within K9, making troubleshooting easier
  - Added retry mechanism for responses containing rate limit messages, improving resilience
  - K9 popover can now be resized by users for better control over interface layout
  - K9 has knowledge of visible and hidden nodes and edges in the graph
  - Added node selection action badges for improved interaction feedback
  - Chat window now scrolls to the top of new K9 messages
  - Fixed issue where badges can't select records from indices that have certain characters like `:`
  - Fixed graph serialization issues for nodes with array fields
  - Fixed error when Siren AI plugin is disabled via configuration

## 1.4.0

- New features
  - K9 can now perform global searches, searching relevant entity tables with the appropriate dynamic filters <br>
    Clicking on the search action in the conversation window allows you to review the parameters K9 used and the results it got back
  - K9 can create new graphs from search results and other data
  - K9 can add nodes, select nodes and group/ungroup nodes in graphs
  - K9 can add nodes to unopened saved graphs
  - K9 can see results from searches you make in the Search app and use them to perform actions (e.g. creating a graph)
  - Ollama can now use tools to perform actions like Azure and OpenAI

- Improvements
  - You can now define a timeout for LLMs in the Investigate server config
  - When K9 fails to perform an action, the error message can be seen in the conversation history
  - K9 can understand grouped edges in the graph
  - K9 can now see record data used in record-as-relation edges
  - Graph reports now display clickable badges when referencing records to help you find them in the graph
  - Updated default user prompt in advanced settings to improve K9's assistive behaviour
  - Various bug fixes and robustness improvements
  - K9 now wags his tail when generating a response.

## 1.3.3

- Fixed an issue where K9 could not see selected nodes in the serialized graph
- Fixed an issue where K9 could not see grouped edges in the graph

## 1.3.2

- Fixed issue where K9 could not see records-as-relations from dataspaces other than HOME
- Minor documentation improvements

## 1.3.1

- Further optimization to the amount of graph data sent to the LLM
- Fixed incorrect graph edge data being sent to the LLM
- Fixed aggregated relations not being seen by the LLM
- Added doc section describing what graph data is used
- Fixed K9 chat window not scrolling to the bottom when new messages are sent/received on Firefox

## 1.3.0

- K9 chat and report generation prompts can now be customized in the advanced settings
- Graph serialization has been turbo-charged, so now graphs up to three times larger can be sent to the LLM
- Minor doc improvements
- Fixed issue where references to EIDs in the graph aren't clickable
- Fixed issue where EIDs couldn't be styled by K9 Chat Companion

## 1.2.0

- K9 improvements
    - References to documents in K9's messages are now clickable and will open in the record viewer
    - Support for styling edges in the graph
    - Support for local nodes in graphs
    - Emoticons are no longer converted to emojis :)
- Minor UI improvements
- Improved error messages
    - When graph is too large
    - When generated graph report can not be downloaded
- Documentation fixes
    - Fixed some scripting examples

## 1.1.0

- K9 Companion now available!
    - Chat with the LLM from the Investigate UI
    - Graph-aware: You can ask questions about the graph you're looking at
    - K9 can set node styles in response to your questions
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

- Generate downoadable reports using AI from the graph browser
- Siren scripting API methods for sending messages and generating reports
- Support for OpenAI, Azure OpenAI, Ollama and AWS Bedrock
- Permissions for configuraing access to Siren AI features
- Support for auditing LLM queries
