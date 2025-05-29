---
title: PageInfo.GetDotNetPaperSize
linktitle: GetDotNetPaperSize
articleTitle: GetDotNetPaperSize
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetDotNetPaperSize في PageInfo، المصممة لاسترداد كائن PaperSize المثالي بسهولة لطباعة الصفحات بسلاسة.
type: docs
weight: 80
url: /ar/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

يحصل علىPaperSize الكائن المناسب للطباعة الصفحة التي يمثلها هذا[`PageInfo`](../) .

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | أحجام الورق المتوفرة. |

### قيمة الإرجاع

كائن يمكنك استخدامه في إطار عمل الطباعة .NET لتحديد حجم الورق.

## أمثلة

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
    /// يقوم بتهيئة نطاق الصفحات التي سيتم طباعتها وفقًا لاختيار المستخدم.
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
     /// يتم استدعاؤها قبل طباعة كل صفحة.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // يمكن أن يحتوي مستند Microsoft Word واحد على أقسام متعددة تحدد الصفحات بأحجام مختلفة،
         // الاتجاهات، وصواني الورق. يستدعي إطار عمل الطباعة .NET هذا الكود قبل
        // تتم طباعة كل صفحة، مما يمنحنا فرصة لتحديد كيفية طباعة الصفحة الحالية.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // يقوم Microsoft Word بتخزين مصدر الورق (درج الطابعة) لكل قسم كقيمة خاصة بالطابعة.
        // للحصول على قيمة الدرج الصحيحة، ستحتاج إلى استخدام خاصية "RawKind"، والتي يجب أن تقوم الطابعة الخاصة بك بإرجاعها.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// يتم استدعاء كل صفحة لتقديمها للطباعة.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // يقوم محرك العرض Aspose.Words بإنشاء صفحة مرسومة من الأصل (x = 0، y = 0) للورقة.
        // سيكون هناك هامشٌ ثابتٌ في الطابعة، والذي سيُطبع كل صفحة. نحتاج إلى تعويضه بهذا الهامش الثابت.
        float hardOffsetX, hardOffsetY;

        // فيما يلي طريقتان لتعيين هامش ثابت.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - عبر خاصية "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - استخدام قيمنا الخاصة، إذا كانت خاصية "PageSettings" غير متوفرة.
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

* class [PageInfo](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
