---
title: Landscape
second_title: Aspose.Words لمراجع .NET API
description: إرجاع صحيح إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة أفقيًا.
type: docs
weight: 20
url: /ar/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

إرجاع صحيح إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة أفقيًا.

```csharp
public bool Landscape { get; }
```

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

يوضح كيفية تخصيص طباعة مستندات Aspose.Words.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// يحدد حجم الورق والاتجاه ودرج الورق المناسب عند الطباعة.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// يقوم بتهيئة نطاق الصفحات التي ستتم طباعتها وفقًا لاختيار المستخدم.
    /// </summary>
    protected override void OnBeginPrint(PrintEventArgs e)
    {
        base.OnBeginPrint(e);

        switch (PrinterSettings.PrintRange)
        {
            case System.Drawing.Printing.PrintRange.AllPages:
                mCurrentPage = 1;
                mPageTo = mDocument.PageCount;
                break;
            case System.Drawing.Printing.PrintRange.SomePages:
                mCurrentPage = PrinterSettings.FromPage;
                mPageTo = PrinterSettings.ToPage;
                break;
            default:
                throw new InvalidOperationException("Unsupported print range.");
        }
    }

    /// <summary>
    /// تم الاتصال قبل طباعة كل صفحة. 
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

        // يمكن أن يحتوي مستند Microsoft Word واحد على أقسام متعددة تحدد صفحات بأحجام مختلفة ، 
        // التوجهات وأدراج الورق. يستدعي إطار عمل الطباعة .NET هذا الرمز من قبل 
        // تتم طباعة كل صفحة ، مما يمنحنا فرصة لتحديد كيفية طباعة الصفحة الحالية.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // يقوم Microsoft Word بتخزين مصدر الورق (علبة الطابعة) لكل قسم كقيمة خاصة بالطابعة.
        // للحصول على قيمة العلبة الصحيحة ، ستحتاج إلى استخدام خاصية "RawKind" ، والتي يجب أن تقوم الطابعة بإرجاعها.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
    /// تم استدعاء كل صفحة لتقديمها للطباعة. 
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Aspose.Words محرك تقديم الكلمات يُنشئ صفحة مأخوذة من أصل الورقة (x = 0، y = 0).
        // سيكون هناك هامش صلب في الطابعة ، والذي سيعرض كل صفحة. نحن بحاجة لتعويض ذلك الهامش الصعب.
        float hardOffsetX, hardOffsetY;

        // فيما يلي طريقتان لتعيين هامش صعب.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - عبر خاصية "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - استخدام القيم الخاصة بنا ، في حالة عدم توفر خاصية "PageSettings".
            hardOffsetX = 20;
            hardOffsetY = 20;
        }

        mDocument.RenderToScale(mCurrentPage, e.Graphics, -hardOffsetX, -hardOffsetY, 1.0f);

        mCurrentPage++;
        e.HasMorePages = mCurrentPage <= mPageTo;
    }

    private readonly Document mDocument;
    private int mCurrentPage;
    private int mPageTo;
}
```

### أنظر أيضا

* class [PageInfo](../../pageinfo)
* مساحة الاسم [Aspose.Words.Rendering](../../pageinfo)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
