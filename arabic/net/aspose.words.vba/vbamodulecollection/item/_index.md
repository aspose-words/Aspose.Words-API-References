---
title: VbaModuleCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: VbaModuleCollection ملكية. يسترجع أVbaModule كائن بالفهرس .
type: docs
weight: 20
url: /ar/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

يسترجع أ[`VbaModule`](../../vbamodule/) كائن بالفهرس .

```csharp
public VbaModule this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | الفهرس الصفري للوحدة المراد استردادها. |

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

---

## VbaModuleCollection indexer (2 of 2)

يسترجع أ[`VbaModule`](../../vbamodule/)الكائن بالاسم ، أو Null إذا لم يتم العثور عليه.

```csharp
public VbaModule this[string name] { get; }
```

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


