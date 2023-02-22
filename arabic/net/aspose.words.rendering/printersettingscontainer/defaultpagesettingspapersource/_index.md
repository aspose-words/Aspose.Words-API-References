---
title: PrinterSettingsContainer.DefaultPageSettingsPaperSource
second_title: Aspose.Words لمراجع .NET API
description: PrinterSettingsContainer ملكية. انظرPaperSource منDefaultPageSettings .
type: docs
weight: 20
url: /ar/net/aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/
---
## PrinterSettingsContainer.DefaultPageSettingsPaperSource property

انظرPaperSource منDefaultPageSettings .

```csharp
public PaperSource DefaultPageSettingsPaperSource { get; }
```

### أمثلة

يوضح كيفية الوصول إلى مصادر الورق وأحجام الطابعة الخاصة بك وسردها.

```csharp
// يحتوي "PrinterSettingsContainer" على كائن "PrinterSettings" ،
// الذي يحتوي على بيانات فريدة لمختلف برامج تشغيل الطابعة.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// تحتوي خاصية "أحجام الورق" على قائمة بأحجام الورق لتوجيه الطابعة لاستخدامها.
// يحتوي كل من PrinterSource و PrinterSize على خاصية "RawKind" ،
// الذي يعادل نوع الورق المدرج في تعداد PaperSourceKind.
// إذا كان هناك مصدر ورق بنفس قيمة "RawKind" مثل تلك الخاصة بصفحة الطباعة ،
// ستطبع الطابعة الصفحة باستخدام مصدر الورق وحجمه المقدمين.
// خلاف ذلك ، ستقوم الطابعة افتراضيًا بالمصدر المعين بواسطة خاصية "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### أنظر أيضا

* class [PrinterSettingsContainer](../)
* مساحة الاسم [Aspose.Words.Rendering](../../printersettingscontainer/)
* المجسم [Aspose.Words](../../../)


