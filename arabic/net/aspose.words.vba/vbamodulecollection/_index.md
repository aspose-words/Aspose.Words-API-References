---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Vba.VbaModuleCollection، وهي أداة أساسية لإدارة كائنات VbaModule بكفاءة في أتمتة المستندات.
type: docs
weight: 7410
url: /ar/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

يمثل مجموعة من[`VbaModule`](../vbamodule/) الأشياء.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات الماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | يعيد عدد وحدات VBA في المجموعة. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | يسترجع[`VbaModule`](../vbamodule/) الكائن حسب index. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | يضيف وحدة إلى المجموعة. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | يزيل الوحدة المحددة من المجموعة. |

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

* class [VbaModule](../vbamodule/)
* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)
