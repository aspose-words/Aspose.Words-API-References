---
title: Landscape
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает значение true если ориентация страницы указанная в документе для этой страницы является альбомной.
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

Возвращает значение true, если ориентация страницы, указанная в документе для этой страницы, является альбомной.

```csharp
public bool Landscape { get; }
```

### Примеры

Показывает, как печатать информацию о размере и ориентации каждой страницы в документе Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// В первом разделе 2 страницы. Каждому из них мы назначим отдельный лоток для бумаги принтера,
// чей номер будет соответствовать типу источника бумаги. Эти источники и их виды будут различаться
// в зависимости от установленного драйвера принтера.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Каждая страница имеет объект PageInfo, индексом которого является номер соответствующей страницы.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Печатаем ориентацию и размеры страницы.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Печать информации об исходном лотке.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
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
/// Выбор подходящего размера бумаги, ориентации и лотка для бумаги при печати.
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

        // Один документ Microsoft Word может иметь несколько разделов, в которых указаны страницы разных размеров, 
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

* class [PageInfo](../)
* пространство имен [Aspose.Words.Rendering](../../pageinfo/)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
