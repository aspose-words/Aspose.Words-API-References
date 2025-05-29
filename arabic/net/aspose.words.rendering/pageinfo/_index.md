---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Rendering.PageInfo، التي توفر تفاصيل أساسية حول كل صفحة من صفحات المستند، مما يعزز تجربة عرض المستند لديك.
type: docs
weight: 5300
url: /ar/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

يمثل معلومات حول صفحة مستند معينة.

لمعرفة المزيد، قم بزيارة[التقديم](https://docs.aspose.com/words/net/rendering/) مقالة توثيقية.

```csharp
public class PageInfo
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | إرجاع`حقيقي` إذا كانت الصفحة تحتوي على محتوى ملون. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | يحصل على ارتفاع الصفحة بالنقاط. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | إرجاع`حقيقي` إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة هو أفقي. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | يحصل على حجم الورق كعدد. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | يحصل على درج الورق (الحاوية) لهذه الصفحة كما هو محدد في المستند. القيمة خاصة بالتنفيذ (الطابعة). |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | يحصل على حجم الصفحة بالنقاط. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | يحصل على عرض الصفحة بالنقاط. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | يحصل علىPaperSize الكائن المناسب للطباعة الصفحة التي يمثلها هذا`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | يحصل علىPaperSource الكائن المناسب للطباعة الصفحة التي يمثلها هذا`PageInfo` . |

## ملاحظات

يمثل عرض الصفحة وارتفاعها المسترجعان بواسطة هذا الكائن الحجم "النهائي" للصفحة، على سبيل المثال، are تم تدويرها بالفعل إلى الاتجاه الصحيح.

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

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)
