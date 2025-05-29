---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words لـ .NET
description: استغل قوة Aspose.Words.Vba.VbaModule للوصول بسلاسة إلى وحدات مشروع VBA. حسّن إنتاجيتك وحسّن أتمتة مستنداتك!
type: docs
weight: 7400
url: /ar/net/aspose.words.vba/vbamodule/
---
## VbaModule class

يوفر الوصول إلى وحدة مشروع VBA.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات الماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public class VbaModule
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [VbaModule](vbamodule/)() | ينشئ وحدة فارغة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | يحصل على اسم وحدة مشروع VBA أو يعينه. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | يحصل على كود مصدر وحدة مشروع VBA أو يعينه. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | يحدد ما إذا كانت الوحدة عبارة عن وحدة إجرائية أو وحدة مستند أو وحدة فئة أو وحدة مصمم. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | يقوم بإجراء نسخة من`VbaModule` . |

## أمثلة

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

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)
