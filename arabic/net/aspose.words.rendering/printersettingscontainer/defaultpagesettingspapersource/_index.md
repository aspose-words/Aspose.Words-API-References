---
title: PrinterSettingsContainer.DefaultPageSettingsPaperSource
linktitle: DefaultPageSettingsPaperSource
articleTitle: DefaultPageSettingsPaperSource
second_title: Aspose.Words لـ .NET
description: PrinterSettingsContainer DefaultPageSettingsPaperSource ملكية. انظرPaperSource لDefaultPageSettings  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/
---
## PrinterSettingsContainer.DefaultPageSettingsPaperSource property

انظرPaperSource لDefaultPageSettings .

```csharp
public PaperSource DefaultPageSettingsPaperSource { get; }
```

## أمثلة

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

* class [PrinterSettingsContainer](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
