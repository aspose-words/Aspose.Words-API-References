---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words لـ .NET
description: استغل قوة فئة Aspose.Words.Vba.VbaProject لإدارة معلومات ووحدات مشروع VBA بسهولة داخل مستنداتك. حسّن أتمتتك اليوم!
type: docs
weight: 7430
url: /ar/net/aspose.words.vba/vbaproject/
---
## VbaProject class

يوفر الوصول إلى معلومات مشروع VBA. يتم تعريف مشروع VBA داخل المستند كمجموعة من وحدات VBA.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات الماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public class VbaProject
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [VbaProject](vbaproject/)() | ينشئ مساحة فارغة`VbaProject` . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | يحصل على صفحة التعليمات البرمجية لمشروع VBA أو يعينها. |
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | يظهر ما إذا كان`VbaProject` محمي بكلمة مرور. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | يظهر ما إذا كان`VbaProject` هل تم التوقيع أم لا. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | إرجاع مجموعة من وحدات مشروع VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | يحصل على اسم مشروع VBA أو يعينه. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | يحصل على مجموعة من مراجع مشروع VBA. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | يقوم بإجراء نسخة من`VbaProject` . |

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
