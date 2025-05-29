---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مشاريع VBA الخاصة بك بسهولة باستخدام طريقة الإضافة VbaModuleCollection، مما يسمح بإضافة وحدات نمطية بسلاسة لتحسين الوظائف.
type: docs
weight: 30
url: /ar/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

يضيف وحدة إلى المجموعة.

```csharp
public void Add(VbaModule vbaModule)
```

## أمثلة

يوضح كيفية إنشاء مشروع VBA باستخدام وحدات الماكرو.

```csharp
Document doc = new Document();

// إنشاء مشروع VBA جديد.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// قم بإنشاء وحدة نمطية جديدة وحدد كود مصدر الماكرو.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

//أضف الوحدة إلى مشروع VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### أنظر أيضا

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
