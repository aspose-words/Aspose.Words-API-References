---
title: Class VbaModuleCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Vba.VbaModuleCollection فصل. يمثل مجموعة منVbaModule الكائنات .
type: docs
weight: 6250
url: /ar/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

يمثل مجموعة من[`VbaModule`](../vbamodule/) الكائنات .

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | إرجاع عدد وحدات VBA النمطية في المجموعة. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | يسترجع أ[`VbaModule`](../vbamodule/) كائن بالفهرس . (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(VbaModule) | يضيف وحدة نمطية إلى المجموعة. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(VbaModule) | يزيل الوحدة النمطية المحددة من المجموعة. |

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

* class [VbaModule](../vbamodule/)
* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)


