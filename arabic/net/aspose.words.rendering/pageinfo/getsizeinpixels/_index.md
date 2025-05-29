---
title: PageInfo.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة PageInfo GetSizeInPixels لحساب حجم صفحتك بدقة بالبكسل استنادًا إلى عامل التكبير والدقة للحصول على عرض مثالي.
type: docs
weight: 90
url: /ar/net/aspose.words.rendering/pageinfo/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| scale | Single | عامل التكبير (1.0 هو 100%). |
| dpi | Single | الدقة (الأفقية والرأسية) لتحويل النقاط إلى بكسل (نقطة لكل بوصة). |

### قيمة الإرجاع

حجم الصفحة بالبكسل.

## أمثلة

يوضح كيفية طباعة معلومات حجم الصفحة والاتجاه لكل صفحة في مستند Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// القسم الأول يتكون من صفحتين. سنخصص لكل صفحة درج ورق طابعة مختلف.
// سيتطابق رقمه مع نوع مصدر الورق. ستختلف هذه المصادر وأنواعها.
// اعتمادًا على برنامج تشغيل الطابعة المثبت.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // تحتوي كل صفحة على كائن PageInfo، والذي يكون فهرسه هو رقم الصفحة المعنية.
    PageInfo pageInfo = doc.GetPageInfo(i);

    //طباعة اتجاه الصفحة وأبعادها.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    //طباعة معلومات الدرج المصدر.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| scale | Single | عامل التكبير (1.0 هو 100%). |
| horizontalDpi | Single | الدقة الأفقية لتحويل النقاط إلى بكسل (نقطة لكل بوصة). |
| verticalDpi | Single | الدقة الرأسية لتحويل النقاط إلى بكسل (نقطة لكل بوصة). |

### قيمة الإرجاع

حجم الصفحة بالبكسل.

## أمثلة

يوضح كيفية طباعة معلومات حجم الصفحة والاتجاه لكل صفحة في مستند Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// القسم الأول يتكون من صفحتين. سنخصص لكل صفحة درج ورق طابعة مختلف.
// سيتطابق رقمه مع نوع مصدر الورق. ستختلف هذه المصادر وأنواعها.
// اعتمادًا على برنامج تشغيل الطابعة المثبت.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // تحتوي كل صفحة على كائن PageInfo، والذي يكون فهرسه هو رقم الصفحة المعنية.
    PageInfo pageInfo = doc.GetPageInfo(i);

    //طباعة اتجاه الصفحة وأبعادها.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    //طباعة معلومات الدرج المصدر.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
