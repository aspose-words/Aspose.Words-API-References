---
title: Enum PdfFontEmbeddingMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.PdfFontEmbeddingMode перечисление. Указывает как Aspose.Words должен встраивать шрифты.
type: docs
weight: 5470
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
| EmbedNonstandard | `1` | Aspose.Words встраивает все шрифты, кроме стандартных шрифтов Windows Arial и Times New Roman. В этом режиме затрагиваются только шрифты Arial и Times New Roman, поскольку MS Word не встраивает только эти шрифты при сохранении документа в PDF. |
| EmbedNone | `2` | Aspose.Words не встраивает шрифты. |

### Примеры

Показывает, как настроить Aspose.Words для пропуска встраивания шрифтов Arial и Times New Roman в PDF-документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// «Arial» — стандартный шрифт, а «Courier New» — нестандартный шрифт.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства «EmbedFullFonts» значение «true», чтобы встроить каждый глиф каждого встроенного шрифта в выходной PDF-файл.
options.EmbedFullFonts = true;

// Установите для свойства FontEmbeddingMode значение «EmbedAll», чтобы встроить все шрифты в выходной PDF-файл.
// Установите для свойства FontEmbeddingMode значение «EmbedNonstandard», чтобы разрешить встраивание только нестандартных шрифтов в выходной PDF-файл.
// Установите для свойства FontEmbeddingMode значение «EmbedNone», чтобы не встраивать шрифты в выходной PDF-файл.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
    case PdfFontEmbeddingMode.EmbedAll:
        Assert.That(1000000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNonstandard:
        Assert.That(480000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNone:
        Assert.That(4255, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


