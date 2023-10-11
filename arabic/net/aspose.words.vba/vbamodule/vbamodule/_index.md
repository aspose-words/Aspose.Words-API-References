---
title: VbaModule.VbaModule
second_title: Aspose.Words لمراجع .NET API
description: VbaModule البناء. إنشاء وحدة فارغة.
type: docs
weight: 10
url: /ar/net/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule constructor

إنشاء وحدة فارغة.

```csharp
public VbaModule()
```

### أمثلة

يوضح كيفية إنشاء مشروع VBA باستخدام وحدات الماكرو.

```csharp
Document doc = new Document();

// إنشاء مشروع VBA جديد.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// أنشئ وحدة نمطية جديدة وحدد كود مصدر الماكرو.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// أضف الوحدة النمطية إلى مشروع VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### أنظر أيضا

* class [VbaModule](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbamodule/)
* المجسم [Aspose.Words](../../../)


