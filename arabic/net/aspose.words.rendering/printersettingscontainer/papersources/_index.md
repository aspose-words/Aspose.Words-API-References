---
title: PrinterSettingsContainer.PaperSources
linktitle: PaperSources
articleTitle: PaperSources
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PaperSources في PrinterSettingsContainer لطباعة سلسة. حسّن إعدادات الطباعة لتحقيق نتائج وكفاءة أفضل!
type: docs
weight: 40
url: /ar/net/aspose.words.rendering/printersettingscontainer/papersources/
---
## PrinterSettingsContainer.PaperSources property

انظرPaperSources .

```csharp
public PaperSourceCollection PaperSources { get; }
```

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

* class [PrinterSettingsContainer](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
