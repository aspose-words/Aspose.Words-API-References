---
title: Class PrinterSettingsContainer
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Rendering.PrinterSettingsContainer فصل. يمثل مخزنًا لبعض معلماتPrinterSettings الكائن.
type: docs
weight: 4580
url: /ar/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

يمثل مخزنًا لبعض معلماتPrinterSettings الكائن.

لمعرفة المزيد، قم بزيارة[طباعة مستند برمجياً أو باستخدام مربعات الحوار](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) مقالة توثيقية.

```csharp
public class PrinterSettingsContainer
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(PrinterSettings) | إنشاء حاوية لـPrinterSettings . |

## الخصائص

| اسم | وصف |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | انظرPaperSource لDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | انظرPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | انظرPaperSources . |

### ملاحظات

الوصول إلى بياناتPrinterSettings يستغرق وقتا طويلا. `PrinterSettingsContainer` تخزين المعلمات منPrinterSettings لذا فإن الطباعة تعمل بشكل أسرع.

### أمثلة

يوضح كيفية الوصول إلى مصادر الورق وأحجامه وإدراجها في الطابعة.

```csharp
// يحتوي "PrinterSettingsContainer" على كائن "PrinterSettings"،
// الذي يحتوي على بيانات فريدة لبرامج تشغيل الطابعة المختلفة.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// تحتوي خاصية "أحجام الورق" على قائمة بأحجام الورق لتوجيه الطابعة لاستخدامها.
// يحتوي كل من PrinterSource وPrinterSize على خاصية "RawKind"،
// والذي يعادل نوع الورق المدرج في تعداد PaperSourceKind.
// إذا كان هناك مصدر ورق له نفس قيمة "RawKind" مثل قيمة صفحة الطباعة،
// ستقوم الطابعة بطباعة الصفحة باستخدام مصدر الورق وحجمه المقدمين.
// بخلاف ذلك، ستنتقل الطابعة افتراضيًا إلى المصدر المعين بواسطة خاصية "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)


