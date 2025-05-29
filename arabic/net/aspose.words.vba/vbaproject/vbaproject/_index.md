---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words لـ .NET
description: أنشئ مشروع Vba جديدًا بسهولة باستخدام أداة البناء لدينا. ابدأ رحلتك البرمجية بمشروع فارغ، وأطلق العنان لإبداعك!
type: docs
weight: 10
url: /ar/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

ينشئ مساحة فارغة[`VbaProject`](../) .

```csharp
public VbaProject()
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

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
