---
title: "Visual Studio Versions - EF6"
author: divega
ms.date: "2016-10-23"
ms.prod: "entity-framework"
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: "article"
ms.assetid: 028FF890-4EDB-4F03-AE53-72F9C33EC92F
caps.latest.revision: 3
---
# Visual Studio Versions

Various samples and walkthroughs across the Entity Framework documentation assume that you are using a recent version of Visual Studio.
However, it is possible to use older versions as long as you take into account some differences:

## Visual Studio 2010

By default, the SQL Server instance available with this version of Visual Studio is SQL Server Express named SQLEXPRESS.
The server section of connection string you should use is ".\\SQLEXPRESS".
Remember to use a verbatim string prefixed with `@` or double back-slashes "\\\\" when specifying a connection string in C# code).
By default, all code generation for this version of Visual Studio is based on EntityObject.
We recommend that you switch the code generation to be based on DbContext by installing the code generation templates.

## Visual Studio 2012

By default, the SQL Server instance available with this version of Visual Studio is a LocalDB instance called v11.0.
The server section of connection string you should use is "(localdb)\\v11.0".
Remember to use a verbatim string prefixed with `@` or double back-slashes "\\\\" when specifying a connection string in C# code).  

## Visual Studio 2013 and newer

By default, the SQL Server instance available with this version of Visual Studio is a LocalDB instance called MSSQLLocalDB.
The server section of connection string you should use is "(localdb)\\MSSQLLocalDB".
Remember to use a verbatim string prefixed with `@` or double back-slashes "\\\\" when specifying a connection string in C# code).  
