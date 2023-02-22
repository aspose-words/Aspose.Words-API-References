---
title: PageInfo.GetSizeInPixels
second_title: Aspose.Words لمراجع .NET API
description: PageInfo طريقة. حساب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.
type: docs
weight: 80
url: /ar/net/aspose.words.rendering/pageinfo/getsizeinpixels/
---
## GetSizeInPixels(float, float) {#getsizeinpixels}

حساب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| scale | Single | عامل التكبير (1.0 هو 100٪). |
| dpi | Single | الدقة (أفقيًا وعموديًا) للتحويل من النقاط إلى البكسل (نقطة في البوصة). |

### قيمة الإرجاع

حجم الصفحة بالبكسل.

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../pageinfo/)
* المجسم [Aspose.Words](../../../)

---

## GetSizeInPixels(float, float, float) {#getsizeinpixels_1}

حساب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| scale | Single | عامل التكبير (1.0 هو 100٪). |
| horizontalDpi | Single | الدقة الأفقية للتحويل من النقاط إلى البكسل (نقاط في البوصة). |
| verticalDpi | Single | الدقة الرأسية للتحويل من النقاط إلى البكسل (نقطة في البوصة). |

### قيمة الإرجاع

حجم الصفحة بالبكسل.

### أمثلة

يوضح كيفية طباعة حجم الصفحة ومعلومات الاتجاه لكل صفحة في مستند Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// يحتوي القسم الأول على صفحتين. سنقوم بتعيين درج ورق طابعة مختلف لكل واحد ،
// الذي سيتطابق رقمه مع نوع مصدر الورق. هذه المصادر وأنواعها سوف تختلف
// اعتمادًا على برنامج تشغيل الطابعة المثبت.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // تحتوي كل صفحة على كائن PageInfo ، والفهرس الخاص به هو رقم الصفحة المعنية.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // اطبع اتجاه الصفحة وأبعادها.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // اطبع معلومات علبة المصدر.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../pageinfo/)
* المجسم [Aspose.Words](../../../)


