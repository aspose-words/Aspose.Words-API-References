---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Rendering.PageInfo, который предоставляет основные сведения о каждой странице документа, улучшая процесс рендеринга документов.
type: docs
weight: 5300
url: /ru/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Представляет информацию о конкретной странице документа.

Чтобы узнать больше, посетите[Рендеринг](https://docs.aspose.com/words/net/rendering/) документальная статья.

```csharp
public class PageInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Возврат`истинный` если страница содержит цветной контент. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Получает высоту страницы в пунктах. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Возврат`истинный` если в документе для этой страницы указана альбомная ориентация. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Получает размер бумаги как перечисление. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Получает лоток для бумаги (корзину) для этой страницы, как указано в документе. Значение зависит от реализации (принтера). |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Получает размер страницы в пунктах. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Получает ширину страницы в пунктах. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | ПолучаетPaperSize объект, подходящий для печати страница, представленная этим`PageInfo` . |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Вычисляет размер страницы в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Вычисляет размер страницы в пикселях для указанного коэффициента масштабирования и разрешения. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | ПолучаетPaperSource объект, подходящий для печати страница, представленная этим`PageInfo` . |

## Примечания

Ширина и высота страницы, возвращаемые этим объектом, представляют собой «окончательный» размер страницы, например, они are уже повернуты в правильную ориентацию.

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

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)
