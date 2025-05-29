---
title: VbaModuleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: تمتع بالوصول إلى كائنات VbaModule بسهولة باستخدام خاصية VbaModuleCollection Item. حسّن مشاريع VBA الخاصة بك بفهرسة سهلة وإدارة مُحسّنة.
type: docs
weight: 20
url: /ar/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

يسترجع[`VbaModule`](../../vbamodule/) الكائن حسب index.

```csharp
public VbaModule this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس يعتمد على الصفر للوحدة التي سيتم استرجاعها. |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

يسترجع[`VbaModule`](../../vbamodule/) الكائن حسب الاسم، أو Null إذا لم يتم العثور عليه.

```csharp
public VbaModule this[string name] { get; }
```

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
