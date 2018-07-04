---
title: "Get started with Entity Framework 6 - EF6"
author: divega
ms.date: "2016-10-23"
ms.prod: "entity-framework"
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: "article"
ms.assetid: 66ce9113-81d2-480f-8c16-d00ec405b2f7
caps.latest.revision: 3
---
# Get started with Entity Framework 6

You can follow these three simple steps: [Decide what EF workflow you want to use](#decide-what-ef-workflow-you-want-to-use), [Get Entity Framework](#get-entity-framework), and read [Working with DbContext](#learn-how-to-work-with-dbcontext).

You can then jump to [Understanding Entity Framework](#understanding-entity-framework) to build a better understanding of what is happening under the hood.

## Decide what EF workflow you want to use

Entity Framework allows you to create a model by writing code or using boxes and lines in the EF Designer. Both of these approaches can be used to target an existing database or create a new database.

Find out about the EF Designer and Code First and which one is best for you:  

|                                           | I just want to write code...                                                                                                                  | I want to use a designer...                                                                                                        |
|:------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| **I am creating a new database**          | [Use **Code First** to define your model in code and then generate a database.](~/ef6/get-started/code-first-to-a-new-database.md)            | [Use **Model First** to define your model using boxes and lines and then generate a database.](~/ef6/get-started/model-first.md)   |
| **I need to access an existing database** | [Use **Code First** to create a code based model that maps to an existing database.](~/ef6/get-started/code-first-to-an-existing-database.md) | [Use **Database First** to create a boxes and lines model that maps to an existing database.](~/ef6/get-started/database-first.md) |

### Watch the video

This short video explains the differences, and how to find the one that is right for you.

**Presented By**: [Rowan Miller](http://romiller.com/)

![WhichWorkflow_Thumb](../media/whichworkflow-thumb.png)
 [WMV](http://download.microsoft.com/download/8/F/8/8F81F4CD-3678-4229-8D79-0C63FFA3C595/HDI_ITPro_Technet_winvideo_ChoseYourWorkflow.wmv) | [MP4](http://download.microsoft.com/download/8/F/8/8F81F4CD-3678-4229-8D79-0C63FFA3C595/HDI_ITPro_Technet_mp4video_ChoseYourWorkflow.m4v) | [WMV (ZIP)](http://download.microsoft.com/download/8/F/8/8F81F4CD-3678-4229-8D79-0C63FFA3C595/HDI_ITPro_Technet_winvideo_ChoseYourWorkflow.zip)

If you still don't feel comfortable deciding, learn both!

## [Get Entity Framework](get-entity-framework.md)
Here you will learn how to add Entity Framework to your applications and, if you want to use the EF Designer, how to get it in Visual Studio.

## [Working with DbContext](working-with-dbcontext.md)
Here you will learn the basics of how to use Entity Framework.

## [Understanding Entity Framework](understanding-ef.md)
Here we will explore more detailed explanations of the basic capabilities, benefits and architecture of EF.
