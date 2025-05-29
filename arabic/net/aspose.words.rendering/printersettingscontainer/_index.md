---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Rendering.PrinterSettingsContainer لإدارة معلمات PrinterSettings بكفاءة، مما يعزز تجربة عرض المستندات لديك.
type: docs
weight: 5310
url: /ar/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

تمثل تخزينًا لبعض معلماتPrinterSettings الكائن.

لمعرفة المزيد، قم بزيارة[طباعة مستند برمجيًا أو باستخدام مربعات الحوار](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) مقالة توثيقية.

```csharp
public class PrinterSettingsContainer
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | ينشئ حاوية لـPrinterSettings . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | انظرPaperSource لDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | انظرPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | انظرPaperSources . |

## ملاحظات

الوصول إلى بياناتPrinterSettings يستغرق وقتا طويلا. `PrinterSettingsContainer` يخزن المعلمات مؤقتًا منPrinterSettings ، حتى تتم الطباعة بشكل أسرع.

## أمثلة

يوضح لك كيفية الوصول إلى مصادر وأحجام ورق الطابعة الخاصة بك وإدراجها.

```csharp
// يحتوي "PrinterSettingsContainer" على كائن "PrinterSettings"،
// والتي تحتوي على بيانات فريدة لبرامج تشغيل الطابعة المختلفة.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// تحتوي خاصية "PaperSizes" على قائمة أحجام الورق التي يجب على الطابعة استخدامها.
// يحتوي كل من PrinterSource وPrinterSize على خاصية "RawKind"،
// وهو ما يعادل نوع الورق المدرج في مجموعة PaperSourceKind.
// إذا كان هناك مصدر ورق بنفس قيمة "RawKind" مثل قيمة صفحة الطباعة،
// ستقوم الطابعة بطباعة الصفحة باستخدام مصدر الورق والحجم المقدمين.
// خلاف ذلك، سيتم تعيين الطابعة افتراضيًا على المصدر المحدد بواسطة الخاصية "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)
