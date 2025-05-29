---
title: VbaModule
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words لـ .NET
description: أنشئ وحدات VBA فارغة بسهولة باستخدام مُنشئ VbaModule. بسّط عملية البرمجة لديك وحسّن سير عمل التطوير لديك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

ينشئ وحدة فارغة.

```csharp
public VbaModule()
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

* class [VbaModule](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
