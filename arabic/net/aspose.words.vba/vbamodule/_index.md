---
title: Class VbaModule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Vba.VbaModule فصل. يوفر الوصول إلى وحدة مشروع VBA .
type: docs
weight: 6240
url: /ar/net/aspose.words.vba/vbamodule/
---
## VbaModule class

يوفر الوصول إلى وحدة مشروع VBA .

```csharp
public class VbaModule
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [VbaModule](vbamodule/)() | ينشئ وحدة فارغة . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | الحصول على أو تعيين اسم وحدة مشروع VBA . |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | الحصول على أو تعيين رمز مصدر وحدة مشروع VBA. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | تحديد ما إذا كانت الوحدة النمطية هي وحدة نمطية إجرائية ، أو وحدة مستند ، أو وحدة فئة نمطية ، أو وحدة مصمم. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | يقوم بتنفيذ نسخة من ملف`VbaModule` . |

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

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)


