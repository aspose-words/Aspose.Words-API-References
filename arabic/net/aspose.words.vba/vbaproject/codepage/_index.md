---
title: VbaProject.CodePage
linktitle: CodePage
articleTitle: CodePage
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة خاصية VbaProject CodePage لتحسين إعدادات صفحة التعليمات البرمجية لمشروع VBA الخاص بك لتحسين الأداء والتوافق.
type: docs
weight: 20
url: /ar/net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

يحصل على صفحة التعليمات البرمجية لمشروع VBA أو يعينها.

```csharp
public int CodePage { get; set; }
```

## ملاحظات

يرجى ملاحظة أن VBA هي ميزة سابقة لـ Unicode وعليك تعيين صفحة التعليمات البرمجية المناسبة صراحةً للحفاظ على مجموعات الأحرف الإقليمية.

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

* class [VbaProject](../)
* مساحة الاسم [Aspose.Words.Vba](../../../aspose.words.vba/)
* المجسم [Aspose.Words](../../../)
