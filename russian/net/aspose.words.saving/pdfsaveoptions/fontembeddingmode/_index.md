---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontEmbeddingMode PdfSaveOptions для оптимизации внедрения шрифтов в PDF. Улучшите качество и совместимость документа без усилий!
type: docs
weight: 170
url: /ru/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Указывает режим внедрения шрифта.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Примечания

Значение по умолчанию:EmbedAll.

Эта настройка работает только для текста в кодировке ANSI (Windows-1252). Если документ содержит не-ANSI текст, то соответствующие шрифты будут внедрены независимо от этой настройки.

Для соответствия стандартам PDF/A и PDF/UA все шрифты должны быть встроены. EmbedAll значение будет использовано автоматически при сохранении в формате PDF/A и PDF/UA.

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

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
