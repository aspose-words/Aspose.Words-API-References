---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление TxtExportHeadersFootersMode в Aspose.Words улучшает экспорт обычного текста, настраивая обработку верхних и нижних колонтитулов для достижения оптимальных результатов.
type: docs
weight: 6440
url: /ru/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Указывает способ экспорта верхних и нижних колонтитулов в формат обычного текста.

```csharp
public enum TxtExportHeadersFootersMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Верхние и нижние колонтитулы не экспортируются. |
| PrimaryOnly | `1` | Экспортируются только основные верхние и нижние колонтитулы в начале и конце каждого раздела. |
| AllAtEnd | `2` | Все верхние и нижние колонтитулы размещаются после всех разделов в самом конце документа. |

## Примеры

Показывает, как указать способ экспорта верхних и нижних колонтитулов в формат обычного текста.

```csharp
Document doc = new Document();

// Вставить четные и основные верхние/нижние колонтитулы в документ.
// Основные верхние/нижние колонтитулы переопределят четные верхние/нижние колонтитулы.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Вставьте страницы для отображения этих верхних и нижних колонтитулов.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Создаем объект "TxtSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ сохранения документа в виде обычного текста.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Установите свойство "ExportHeadersFootersMode" на "TxtExportHeadersFootersMode.None"
// чтобы не экспортировать верхние/нижние колонтитулы.
// Установите свойство "ExportHeadersFootersMode" на "TxtExportHeadersFootersMode.PrimaryOnly"
// для экспорта только основных верхних/нижних колонтитулов.
// Установите свойство "ExportHeadersFootersMode" на "TxtExportHeadersFootersMode.AllAtEnd"
// для размещения всех верхних и нижних колонтитулов всех разделов в конце документа.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
