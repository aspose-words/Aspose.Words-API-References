---
title: VbaProject.IsSigned
linktitle: IsSigned
articleTitle: IsSigned
second_title: Aspose.Words لـ .NET
description: VbaProject IsSigned ملكية. يظهر ما إذا كانVbaProject تم التوقيع أم لا في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.vba/vbaproject/issigned/
---
## VbaProject.IsSigned property

يظهر ما إذا كان[`VbaProject`](../) تم التوقيع أم لا.

```csharp
public bool IsSigned { get; }
```

## أمثلة

يوضح كيفية الوصول إلى معلومات مشروع VBA الخاص بالمستند.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// يحتوي مشروع VBA على مجموعة من وحدات VBA.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// قم بتعيين كود مصدر جديد لوحدة VBA. يمكنك الوصول إلى وحدات VBA الموجودة في المجموعة إما عن طريق الفهرس أو بالاسم.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// إزالة وحدة من المجموعة.
vbaModules.Remove(vbaModules[2]);
```

### أنظر أيضا

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
