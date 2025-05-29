---
title: PageInfo.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageInfo SizeInPoints, чтобы легко получить доступ к размеру страницы в пунктах для точного управления макетом и повышения эффективности дизайна.
type: docs
weight: 60
url: /ru/net/aspose.words.rendering/pageinfo/sizeinpoints/
---
## PageInfo.SizeInPoints property

Получает размер страницы в пунктах.

```csharp
public SizeF SizeInPoints { get; }
```

## Примеры

Показывает, как распечатать информацию о размере и ориентации каждой страницы документа Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// В первой секции 2 страницы. Каждой из них мы назначим отдельный лоток для бумаги принтера,
// номер которого будет соответствовать виду источника бумаги. Эти источники и их виды будут различаться
// в зависимости от установленного драйвера принтера.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Каждая страница имеет объект PageInfo, индекс которого — номер соответствующей страницы.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Распечатать ориентацию и размеры страницы.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Распечатать информацию об исходном лотке.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Смотрите также

* class [PageInfo](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
