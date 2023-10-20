---
title: PageInfo.HeightInPoints
linktitle: HeightInPoints
articleTitle: HeightInPoints
second_title: Aspose.Words для .NET
description: PageInfo HeightInPoints свойство. Получает высоту страницы в пунктах на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.rendering/pageinfo/heightinpoints/
---
## PageInfo.HeightInPoints property

Получает высоту страницы в пунктах.

```csharp
public float HeightInPoints { get; }
```

## Примеры

Показывает, как распечатать информацию о размере и ориентации страницы для каждой страницы документа Word.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Первый раздел состоит из 2 страниц. Каждому из них мы назначим отдельный лоток для бумаги для принтера,
// номер которого будет соответствовать типу бумажного источника. Эти источники и их виды будут различаться.
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

    // Распечатываем ориентацию и размеры страницы.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Распечатываем информацию об исходном лотке.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### Смотрите также

* class [PageInfo](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
