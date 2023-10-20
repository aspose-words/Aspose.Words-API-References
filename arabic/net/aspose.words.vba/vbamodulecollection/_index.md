---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Vba.VbaModuleCollection فصل. يمثل مجموعة منVbaModule الكائنات في C#.
type: docs
weight: 6560
url: /ar/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

يمثل مجموعة من[`VbaModule`](../vbamodule/) الكائنات.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات ماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | إرجاع عدد وحدات VBA في المجموعة. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | يسترد أ[`VbaModule`](../vbamodule/) كائن حسب الفهرس. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | إضافة وحدة إلى المجموعة. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | إزالة الوحدة المحددة من المجموعة. |

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

* class [VbaModule](../vbamodule/)
* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)
