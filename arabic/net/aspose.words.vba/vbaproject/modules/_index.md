---
title: VbaProject.Modules
second_title: Aspose.Words لمراجع .NET API
description: VbaProject ملكية. إرجاع مجموعة من الوحدات النمطية لمشروع VBA .
type: docs
weight: 40
url: /ar/net/aspose.words.vba/vbaproject/modules/
---
## VbaProject.Modules property

إرجاع مجموعة من الوحدات النمطية لمشروع VBA .

```csharp
public VbaModuleCollection Modules { get; }
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

* class [VbaModuleCollection](../../vbamodulecollection/)
* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../vbaproject/)
* المجسم [Aspose.Words](../../../)


