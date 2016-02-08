# Messy
Message based DDD + CQRS + EventSourcing bootstrap library

Consists of next projects:
## Messy 
Base classes and interfaces for
* Domain-driven-development (Entity, Value object, Aggregate, Bounded context, Event types, Messaging, Message bus),
* CQRS (Command, Query, Validation), 
* Event sourcing (Domain event, Events router, Database context)
* General purpose (Serialization, Logging, Identifier generation)
* Data structures (Id collection, Range, Series)

##### Depends on packages:
* Autofac
* NLog
* Newtonsoft.Json


## Messy.AdoPersistence
Database access based on ado.net capabilities. Allows to use sql migrations and provides some helper methods for quering and execution stored procedures

##### Depends on packages:
* Autofac
* Dapper
* DbUp


## Messy.EFPersistence
Simple database access based on configured Entity Framework. Added custom naming convention. Removed pluralization and cascade delete conventions. Lazy loading turned off. Auto-import of configuration classes (inherited from EntityTypeConfiguration)

##### Depends on packages:
* Entity Framework

## Messy.EventSourcingPersistence
Implementation of event-sourcing database context interfaces from Messy with the help of Messy.AdoPersistence. Implements simple and batch data context. Contains migrations for events and snapshot tables.

##### Depends on packages:
* Autofac
* Messy.AdoPersistence
