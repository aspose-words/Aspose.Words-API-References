---
title: PageInfo.PaperSize
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageInfo PaperSize لاسترجاع أحجام الورق بسهولة كعدد. حسّن قدرات الطباعة لديك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.rendering/pageinfo/papersize/
---
## PageInfo.PaperSize property

يحصل على حجم الورق كعدد.

```csharp
public PaperSize PaperSize { get; }
```

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

* enum [PaperSize](../../../aspose.words/papersize/)
* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
