---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор PdfSaveOptions, разработанный для легкой инициализации и сохранения ваших документов в высококачественном формате PDF. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в Pdf формат.

```csharp
public PdfSaveOptions()
```

## Примеры

Показывает, как включить или отключить поднабор при внедрении шрифтов во время рендеринга документа в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Настраиваем источники шрифтов, чтобы гарантировать, что у нас есть доступ к обоим шрифтам в этом документе.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Поскольку наш документ содержит пользовательский шрифт, его внедрение в выходной документ может быть желательным.
// Установите свойство «EmbedFullFonts» в значение «true», чтобы встроить каждый глиф каждого встроенного шрифта в выходной PDF-файл.
// Размер документа может стать очень большим, но мы сможем в полной мере использовать все шрифты, если отредактируем PDF-файл.
// Установите свойство "EmbedFullFonts" в значение "false", чтобы применить поднабор к шрифтам, сохраняя только глифы
// который использует документ. Файл будет значительно меньше,
// но нам может понадобиться доступ к любым пользовательским шрифтам, если мы будем редактировать документ.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Восстановить исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
