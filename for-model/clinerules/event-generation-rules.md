---
alwaysApply: true
---
When generating code based on event stickers, please follow these requirements:

1. Reference Metadata
Events use metadata under 'events', and through name and fieldDescriptors, events are published when business logic processing is completed or files are generated accordingly.

2. File Creation Criteria
Event files are created based on event stickers.

Event.java
Filename: Event sticker name.java
Structure:

- fieldDescriptors declaration
- Constructor that takes an Aggregate as a parameter
- Default constructor declaration

Additionally, code declaration is required to publish the Event after the business logic of the Aggregate's port Method is processed