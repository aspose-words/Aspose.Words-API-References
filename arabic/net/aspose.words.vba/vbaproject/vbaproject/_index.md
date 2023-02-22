---
title: VbaProject.VbaProject
second_title: Aspose.Words لمراجع .NET API
description: VbaProject البناء. ينشئ مشروع VbaProject فارغًا .
type: docs
weight: 10
url: /ar/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

ينشئ مشروع VbaProject فارغًا .

```csharp
public VbaProject()
```

### أمثلة

يوضح كيفية إنشاء مشروع VBA باستخدام وحدات الماكرو.

```csharp
Document doc = new Document();

// إنشاء مشروع VBA جديد.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// إنشاء وحدة نمطية جديدة وتحديد شفرة مصدر الماكرو.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// أضف الوحدة إلى مشروع VBA.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### أنظر أيضا

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbaproject/)
* المجسم [Aspose.Words](../../../)


