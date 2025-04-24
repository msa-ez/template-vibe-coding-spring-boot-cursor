---
alwaysApply: true
---
Code generated based on aggregate stickers must follow these requirements:

1. Reference Metadata
Aggregates should be generated based on metadata in the 'aggregates' section, primarily using fieldDescriptors that represent aggregate attributes, and the class diagram relationships (Enumeration, ValueObject, Entity) that exist in aggregateRoot.entities.relations.

2. File Generation Standards
Aggregate-based Root files and Repository files are generated.

AggregateRoot.java
Filename: AggregateName.java
Structure:
- Property declarations based on fieldDescriptors
- lifeCycle(Only generate when the command's metadata isRestRepository is false.)
- Declaration of business logic methods in the inbound adapter (extended API controller, eventListener policyHandler) that publishes events

Repository.java
Filename: AggregateName + Repository.java
Structure:
- Extends JPARepository
- When parameters from views or ReadModels exist, write query statements referencing queryOption