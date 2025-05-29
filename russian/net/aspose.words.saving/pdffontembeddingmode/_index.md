---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PdfFontEmbeddingMode для оптимального внедрения шрифтов в PDF-файлы. Улучшите качество документа и обеспечьте единообразное отображение текста.
type: docs
weight: 6260
url: /ru/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Указывает, как Aspose.Words должен встраивать шрифты.

```csharp
public enum PdfFontEmbeddingMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words встраивает все шрифты. |
| EmbedNonstandard | `1` | Aspose.Words встраивает все шрифты, за исключением стандартных шрифтов Windows Arial и Times New Roman. В этом режиме затрагиваются только шрифты Arial и Times New Roman, поскольку MS Word не встраивает только эти шрифты при сохранении документа в формате PDF. |
| EmbedNone | `2` | Aspose.Words не встраивает шрифты. |

## Примеры

Показывает, как настроить Aspose.Words так, чтобы он не встраивал шрифты Arial и Times New Roman в PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// «Arial» — стандартный шрифт, а «Courier New» — нестандартный шрифт.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Установите свойство «EmbedFullFonts» в значение «true», чтобы встроить каждый глиф каждого встроенного шрифта в выходной PDF-файл.
options.EmbedFullFonts = true;
// Установите свойство «FontEmbeddingMode» на «EmbedAll», чтобы встроить все шрифты в выходной PDF-файл.
// Установите свойство «FontEmbeddingMode» на «EmbedNonstandard», чтобы разрешить встраивание только нестандартных шрифтов в выходной PDF-файл.
// Установите свойство «FontEmbeddingMode» на «EmbedNone», чтобы не встраивать шрифты в выходной PDF-файл.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
