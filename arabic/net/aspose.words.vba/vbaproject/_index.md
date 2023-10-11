---
title: Class VbaProject
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Vba.VbaProject فصل. يوفر الوصول إلى معلومات مشروع VBA. يتم تعريف مشروع VBA الموجود داخل المستند على أنه مجموعة من وحدات VBA.
type: docs
weight: 6580
url: /ar/net/aspose.words.vba/vbaproject/
---
## VbaProject class

يوفر الوصول إلى معلومات مشروع VBA. يتم تعريف مشروع VBA الموجود داخل المستند على أنه مجموعة من وحدات VBA.

لمعرفة المزيد، قم بزيارة[العمل مع وحدات ماكرو VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) مقالة توثيقية.

```csharp
public class VbaProject
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [VbaProject](vbaproject/)() | إنشاء فراغ`VbaProject` . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | الحصول على أو تعيين صفحة التعليمات البرمجية لمشروع VBA. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | يظهر ما إذا كان`VbaProject` تم التوقيع أم لا. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | إرجاع مجموعة وحدات مشروع VBA. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | الحصول على اسم مشروع VBA أو تعيينه. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | الحصول على مجموعة من مراجع مشروع VBA. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | ينفذ نسخة من`VbaProject` . |

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

* مساحة الاسم [Aspose.Words.Vba](../../aspose.words.vba/)
* المجسم [Aspose.Words](../../)


