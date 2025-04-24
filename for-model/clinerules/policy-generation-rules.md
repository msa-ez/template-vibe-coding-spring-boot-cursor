---
alwaysApply: true
---
When generating code based on policy stickers, please follow these requirements:

1. Reference Metadata and Roles

It processes domain events defined in the policies.incomingRelations.source resource of the model metadata. It receives domain events using KafkaListener and generates the received domain event code.
A port method should be declared within the Aggregate Root Entity with the Policy name, and business logic should be implemented by passing the received event.

2. File Creation Criteria
PolicyHandler.java file is created based on policy stickers.

PolicyHandler.java
Filename: PolicyHandler.java
Structure:

- Declaration of events being listened to
- Declaration of connected Policies according to event declarations
- Call to the port method of the Aggregate generated based on the Policy
- Default generation handling if no policies exist