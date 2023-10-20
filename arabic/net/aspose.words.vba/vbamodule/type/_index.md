---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: VbaModule Type ملكية. يحدد ما إذا كانت الوحدة هي وحدة إجرائية أو وحدة مستند أو وحدة فئة أو وحدة مصمم في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

يحدد ما إذا كانت الوحدة هي وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم.

```csharp
public VbaModuleType Type { get; set; }
```

## أمثلة

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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
