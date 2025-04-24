---
alwaysApply: true
---
When generating code based on command stickers, please follow these requirements:

1. Reference Metadata
Commands use metadata under 'commands', and depending on whether isRestRepository is true or false, it determines whether to use basic CRUD API or Extended API. Additionally, when using Extended API, a command file corresponding to the DTO should be generated through fieldDescriptors.

2. File Creation Criteria
Command and Controller files are created under domain and infra directories based on command stickers.

Command.java
Filename: Command sticker name + Command.java
Creation condition: When isRestRepository is false
Structure:
- fieldDescriptors declaration

Controller.java
Filename: Aggregate sticker name + Controller.java
Structure:
- Declaration to enable CRUD operations from the basic Repository
- If there are commands using extended api, generate extended api code based on controllerInfo and the created Command file
- For default api, just declare in the basic structure
- All of the above requirements should be generated in a single Controller.java file.
