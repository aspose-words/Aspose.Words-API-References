---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words для .NET
description: PdfSaveOptions FontEmbeddingMode свойство. Определяет режим внедрения шрифта на С#.
type: docs
weight: 170
url: /ru/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Определяет режим внедрения шрифта.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Примечания

Значение по умолчанию:EmbedAll.

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Если документ содержит текст , отличный от ANSI, соответствующие шрифты будут встроены независимо от этого параметра.

Для соответствия PDF/A и PDF/UA необходимо встроить все шрифты. EmbedAll значение будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

## Примеры

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

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
