---
title: Landscape
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает true если ориентация страницы указанная в документе для этой страницы является альбомной.
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

Возвращает true, если ориентация страницы, указанная в документе для этой страницы, является альбомной.

```csharp
public bool Landscape { get; }
```

### Примеры

Показывает, как печатать информацию о размере и ориентации каждой страницы документа Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Выбирает подходящий размер бумаги, ориентацию и лоток для бумаги при печати.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
     /// Инициализирует диапазон страниц для печати в соответствии с выбором пользователя.
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
     /// Вызывается перед печатью каждой страницы. 
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Один документ Microsoft Word может иметь несколько разделов, в которых указаны страницы разного размера, 
         // ориентации и лотки для бумаги. Платформа печати .NET вызывает этот код перед 
         // печатается каждая страница, что дает нам возможность указать, как печатать текущую страницу.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

         // Microsoft Word сохраняет источник бумаги (лоток принтера) для каждой секции как значение для конкретного принтера.
         // Чтобы получить правильное значение лотка, вам нужно будет использовать свойство "RawKind", которое должен возвращать ваш принтер.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Вызывается для каждой страницы, чтобы отобразить ее для печати. 
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

         // Механизм рендеринга Aspose.Words создает страницу, нарисованную из исходной точки (x = 0, y = 0) бумаги.
        // В принтере будет жесткое поле, которое будет отображать каждую страницу. Нам нужно компенсировать эту жесткую маржу.
        float hardOffsetX, hardOffsetY;

         // Ниже приведены два способа установки жесткого поля.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
             // 1 - Через свойство "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
             // 2 - Используя собственные значения, если свойство "PageSettings" недоступно.
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

Показывает, как настроить печать документов Aspose.Words.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Выбирает подходящий размер бумаги, ориентацию и лоток для бумаги при печати.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
     /// Инициализирует диапазон страниц для печати в соответствии с выбором пользователя.
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
     /// Вызывается перед печатью каждой страницы. 
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Один документ Microsoft Word может иметь несколько разделов, в которых указаны страницы разного размера, 
         // ориентации и лотки для бумаги. Платформа печати .NET вызывает этот код перед 
         // печатается каждая страница, что дает нам возможность указать, как печатать текущую страницу.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

         // Microsoft Word сохраняет источник бумаги (лоток принтера) для каждой секции как значение для конкретного принтера.
         // Чтобы получить правильное значение лотка, вам нужно будет использовать свойство "RawKind", которое должен возвращать ваш принтер.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Вызывается для каждой страницы, чтобы отобразить ее для печати. 
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

         // Механизм рендеринга Aspose.Words создает страницу, нарисованную из исходной точки (x = 0, y = 0) бумаги.
        // В принтере будет жесткое поле, которое будет отображать каждую страницу. Нам нужно компенсировать эту жесткую маржу.
        float hardOffsetX, hardOffsetY;

         // Ниже приведены два способа установки жесткого поля.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
             // 1 - Через свойство "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
             // 2 - Используя собственные значения, если свойство "PageSettings" недоступно.
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

### Смотрите также

* class [PageInfo](../../pageinfo)
* пространство имен [Aspose.Words.Rendering](../../pageinfo)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
