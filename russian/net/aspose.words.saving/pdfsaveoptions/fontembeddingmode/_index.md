---
title: PdfSaveOptions.FontEmbeddingMode
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Определяет режим внедрения шрифта.
type: docs
weight: 140
url: /ru/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Определяет режим внедрения шрифта.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

### Примечания

Значение по умолчаниюEmbedAll.

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Если документ содержит текст, отличный от ANSI, соответствующие шрифты будут внедрены независимо от этого параметра.

Соответствие PDF/A и PDF/UA требует, чтобы все шрифты были встроены. EmbedAll значение будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

### Примеры

Показывает, как настроить Aspose.Words, чтобы пропустить встраивание шрифтов Arial и Times New Roman в документ PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// «Arial» — стандартный шрифт, «Courier New» — нестандартный шрифт.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства "EmbedFullFonts" значение "true", чтобы встроить каждый глиф каждого встроенного шрифта в выходной PDF-файл.
options.EmbedFullFonts = true;

// Установите для свойства «FontEmbeddingMode» значение «EmbedAll», чтобы встроить все шрифты в выходной PDF-файл.
// Установите для свойства «FontEmbeddingMode» значение «EmbedNonstandard», чтобы разрешить встраивание только нестандартных шрифтов в выходной PDF-файл.
// Установите для свойства «FontEmbeddingMode» значение «EmbedNone», чтобы не встраивать какие-либо шрифты в выходной PDF-файл.
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
        Assert.That(4217, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Смотрите также

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


