---
title: VbaModuleCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: VbaModuleCollection ملكية. يسترد أVbaModule كائن حسب الفهرس.
type: docs
weight: 20
url: /ar/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

يسترد أ[`VbaModule`](../../vbamodule/) كائن حسب الفهرس.

```csharp
public VbaModule this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | الفهرس الصفري للوحدة المطلوب استردادها. |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbamodulecollection/)
* المجسم [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

يسترد أ[`VbaModule`](../../vbamodule/) كائن بالاسم، أو Null إذا لم يتم العثور عليه.

```csharp
public VbaModule this[string name] { get; }
```

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbamodulecollection/)
* المجسم [Aspose.Words](../../../)


