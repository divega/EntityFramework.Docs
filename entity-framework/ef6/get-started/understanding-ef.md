---
title: "Understanding Entity Framework - EF6"
author: divega
ms.date: "2016-10-23"
ms.prod: "entity-framework"
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: "article"
ms.assetid: 4ab0958b-e440-494e-8a09-83ee7f400a7a
caps.latest.revision: 3
---
# Understanding Entity Framework
Entity Framework is an object-relational mapper (O/RM) that enables developers to interact with data stored in a relational database by manipulating the application's domain objects.
For example, using Entity Framework you can work with data in the form of domain objects and properties, such as _customers_ and _customer addresses_ , using familiar object-oriented techniques and without having to concern yourself with the underlying database tables and columns where this data is stored.

EF reduces the impedance mismatch between the object-oriented world of .NET Framework developers and the world of relational databases.
Developers can work at a higher level of abstraction when they deal with data, and can create and maintain data-oriented applications with less code than in traditional applications.
A large portion of the data access "plumbing" code that developers usually need to write is eliminated.

The Entity Framework's O/RM implementation provides services like change tracking, identity resolution, lazy loading, and query translation so that developers can focus on their application-specific business logic rather than the data access fundamentals.
Thanks to the query translation capabilities, developers issue queries using Language INtegrated Query (LINQ) or Entity SQL (E-SQL), then retrieve and manipulate query results as strongly typed objects.

## High-level capabilities of EF6   

- Entity Framework works with a variety of database servers (including SQL Server, Oracle, and DB2)  
- Includes a rich mapping engine that can handle a wide variety of database schemas and works well with stored procedures  
- Provides integrated Visual Studio tools to visually create entity models and to auto-generate models from an existing database.
New databases can be deployed from a model, which can also be hand-edited for full control  
- Provides a Code First experience to create entity models using code. Code First can map to an existing database or generate a database from the model.  
- Integrates well into all the .NET Framework application programming models including ASP.NET.
- Builds on the ADO.NET provider model, and takes advantage of existing ADO.NET providers, although Entity Framework providers are required to support the new Entity Framework functionality.

## Benefits of EF6

Using Entity Framework to write data-oriented applications provides the following benefits compared to not using an Object/Relational Mapper:  

- Reduced development time: the framework provides the core data access capabilities so developers can concentrate on application logic.  
- Developers can work in terms of a more application-centric object model, including types with inheritance, complex members, and relationships.
From Entity Framework 4, it also supports Persistence Ignorance through Plain Old CLR Objects (POCO) entities.  
- Applications are freed from hard-coded dependencies on a particular data engine or storage schema by supporting a conceptual model that is independent of the physical/storage model.  
- Mappings between the object model and the storage-specific schema can change without changing the application code.  
- Language-Integrated Query support (called LINQ to Entities) provides IntelliSense and compile-time syntax validation for writing queries against a conceptual model.

# Entity Data Model

The Entity Framework uses the Entity Data Model (EDM) to describe the application-specific object or "conceptual" model against which the developer programs.
The EDM builds on the widely known Entity Relationship model (introduced by Dr. Peter Chen) to raise the abstraction level above logical database schemas.
The EDM was developed with the primary goal of becoming the common data model across a suite of developer and server technologies from Microsoft.
EDM was also used as part of the OData protocol.

## Architecture

There are two major layers in an Entity Framework application:

*   The modeling layer  

*   The object layer  

The modeling layer contains three components:

*   A conceptual model consisting of domain-specific entity types and relationships, based on an [Entity Data Model](http://go.microsoft.com/fwlink/?LinkId=215860) (EDM)  

*   A database schema that defines tables and relationships  

*   A mapping between the conceptual model and the database schema  

Entity Framework uses the mapping component to transform operations against entity objects - such as create, read, update, and delete - into equivalent operations in the database.

The Entity Framework object layer contains typed common language runtime (CLR) objects that reflect the entities and relationships defined in the conceptual model. These objects can be consumed by programming languages.
The exact format of the types is controlled by options you provide to Entity Framework.

## Mapping and Modeling

There are different ways to create the mapping layer and the object layer:

*   You can use Entity Framework Tools to generate your model from an existing database. This generates a default conceptual model and mapping, which you can customize by using the Entity Data Model Designer. You can also use tools to graphically create a conceptual model by using the Entity Data Model Designer, and then generate a database based on the metadata built by the tool from that model.  

*   You can use the Code First development to define your conceptual model in code. The Entity Framework infers the conceptual model based on the object types and additional configurations that you define. The mapping metadata is generated during run time based on a combination of how you defined your domain types and additional configuration information that you provide in code. The model can either be mapped to an existing database or you can generate a new database from your model.  

## Working with Objects

Entity Framework object layer enables you to do the following:

*   Run queries against the conceptual model.  

*   Materialize data returned from the data source as objects.  

*   Track changes that were made to the objects.  

*   Propagate object changes back to the data source.  

*   Bind objects to controls.
