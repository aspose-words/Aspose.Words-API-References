---
title: PageInfo.PaperTray
second_title: Aspose.Words لمراجع .NET API
description: PageInfo ملكية. الحصول على درج الورق الحاوية لهذه الصفحة كما هو محدد في المستند. القيمة خاصة بالتنفيذ الطابعة.
type: docs
weight: 50
url: /ar/net/aspose.words.rendering/pageinfo/papertray/
---
## PageInfo.PaperTray property

الحصول على درج الورق (الحاوية) لهذه الصفحة كما هو محدد في المستند. القيمة خاصة بالتنفيذ (الطابعة).

```csharp
public int PaperTray { get; }
```

### أمثلة

يوضح كيفية طباعة حجم الصفحة ومعلومات الاتجاه لكل صفحة في مستند Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// القسم الأول يحتوي على صفحتين. سنقوم بتخصيص درج ورق طابعة مختلف لكل واحد،
// الذي سيتطابق رقمه مع نوع مصدر الورق. وسوف تختلف هذه المصادر وأنواعها
// اعتمادًا على برنامج تشغيل الطابعة المثبت.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // تحتوي كل صفحة على كائن PageInfo، والفهرس الخاص به هو رقم الصفحة المعنية.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // اطبع اتجاه الصفحة وأبعادها.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // اطبع معلومات الدرج المصدر.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### أنظر أيضا

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../pageinfo/)
* المجسم [Aspose.Words](../../../)


