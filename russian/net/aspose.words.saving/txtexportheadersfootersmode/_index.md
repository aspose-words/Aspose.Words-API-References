---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.TxtExportHeadersFootersMode перечисление. Указывает способ экспорта верхних и нижних колонтитулов в текстовый формат на С#.
type: docs
weight: 5640
url: /ru/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Указывает способ экспорта верхних и нижних колонтитулов в текстовый формат.

```csharp
public enum TxtExportHeadersFootersMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Верхние и нижние колонтитулы не экспортируются. |
| PrimaryOnly | `1` | В начале и конце каждого раздела экспортируются только основные верхние и нижние колонтитулы. |
| AllAtEnd | `2` | Все верхние и нижние колонтитулы размещаются после всех разделов в самом конце документа. |

## Примеры

Показывает, как указать способ экспорта верхних и нижних колонтитулов в текстовый формат.

```csharp
Document doc = new Document();

// Вставляем четные и основные верхние/нижние колонтитулы в документ.
// Первичный верхний/нижний колонтитул переопределяет четные верхние/нижние колонтитулы.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Вставка страниц для отображения этих верхних и нижних колонтитулов.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Создаем объект «TxtSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ сохранения документа в виде открытого текста.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Установите для свойства «ExportHeadersFootersMode» значение «TxtExportHeadersFootersMode.None»
// чтобы не экспортировать верхние/нижние колонтитулы.
// Установите для свойства «ExportHeadersFootersMode» значение «TxtExportHeadersFootersMode.PrimaryOnly»
// чтобы экспортировать только основные верхние и нижние колонтитулы.
// Установите для свойства «ExportHeadersFootersMode» значение «TxtExportHeadersFootersMode.AllAtEnd»
// чтобы разместить все верхние и нижние колонтитулы для всех разделов в конце документа.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Even header\r\n\r\n" +
                        "Primary header\r\n\r\n" +
                        "Even footer\r\n\r\n" +
                        "Primary footer\r\n\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual("Primary header\r\n" +
                        "Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n" +
                        "Primary footer\r\n", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual("Page 1\r\n" +
                        "Page 2\r\n" +
                        "Page 3\r\n", docText);
        break;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
