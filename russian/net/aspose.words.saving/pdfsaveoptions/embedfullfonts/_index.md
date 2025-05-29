---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words для .NET
description: Узнайте, как функция EmbedFullFonts в PdfSaveOptions улучшает ваши PDF-документы, обеспечивая полное внедрение шрифтов для идеального форматирования.
type: docs
weight: 120
url: /ru/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Управляет тем, как шрифты внедряются в результирующие PDF-документы.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`, что означает, что шрифты подмножествуются перед внедрением. Подмножество полезно, если вы хотите сохранить меньший размер выходного файла. Подмножество удаляет все неиспользуемые глифы из шрифта.

Когда это значение установлено на`истинный`, полный файл шрифта встраивается в PDF без подмножества. Это приведет к увеличению выходных файлов, но может быть полезным вариантом, когда вы хотите отредактировать полученный PDF позже (например, добавить больше текста).

Некоторые шрифты имеют большой размер (несколько мегабайт), и их внедрение без subsetting приведет к получению больших выходных документов.

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
