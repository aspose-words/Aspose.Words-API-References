---
title: VbaProject.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة مشروع VBA بسهولة باستخدام خاصية الاسم. تعلم كيفية الحصول على أسماء المشاريع وتعيينها لكتابة برمجية فعّالة!
type: docs
weight: 60
url: /ar/net/aspose.words.vba/vbaproject/name/
---
## VbaProject.Name property

يحصل على اسم مشروع VBA أو يعينه.

```csharp
public string Name { get; set; }
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

يوضح كيفية الوصول إلى معلومات مشروع VBA الخاصة بالمستند.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

//يحتوي مشروع VBA على مجموعة من وحدات VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules;

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// تعيين شيفرة مصدر جديدة لوحدة VBA. يمكنك الوصول إلى وحدات VBA في المجموعة إما عن طريق الفهرس أو الاسم.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// إزالة وحدة من المجموعة.
vbaModules.Remove(vbaModules[2]);
```

### أنظر أيضا

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
