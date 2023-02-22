---
title: VbaModuleCollection.Remove
second_title: Aspose.Words لمراجع .NET API
description: VbaModuleCollection طريقة. يزيل الوحدة النمطية المحددة من المجموعة.
type: docs
weight: 40
url: /ar/net/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection.Remove method

يزيل الوحدة النمطية المحددة من المجموعة.

```csharp
public void Remove(VbaModule module)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| module | VbaModule | الوحدة المراد إزالتها. |

### أمثلة

يوضح كيفية الوصول إلى معلومات مشروع VBA للمستند.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// يحتوي مشروع VBA على مجموعة من وحدات VBA النمطية.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// تعيين رمز مصدر جديد لوحدة VBA. يمكنك الوصول إلى وحدات VBA النمطية في المجموعة إما بالفهرس أو بالاسم.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// إزالة وحدة من المجموعة.
vbaModules.Remove(vbaModules[2]);
```

### أنظر أيضا

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbamodulecollection/)
* المجسم [Aspose.Words](../../../)


