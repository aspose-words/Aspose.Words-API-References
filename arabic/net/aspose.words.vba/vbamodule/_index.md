---
title: Class VbaModule
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Vba.VbaModule فصل. يوفر الوصول إلى وحدة مشروع VBA.
type: docs
weight: 6550
url: /ar/net/aspose.words.vba/vbamodule/
---
## VbaModule class

يوفر الوصول إلى وحدة مشروع VBA.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات ماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public class VbaModule
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [VbaModule](vbamodule/)() | إنشاء وحدة فارغة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | الحصول على اسم الوحدة النمطية لمشروع VBA أو تعيينه. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | الحصول على الكود المصدري لوحدة مشروع VBA أو تعيينه. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | يحدد ما إذا كانت الوحدة هي وحدة إجرائية، أو وحدة مستند، أو وحدة فئة، أو وحدة مصمم. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | ينفذ نسخة من`VbaModule` . |

### أمثلة

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

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)


