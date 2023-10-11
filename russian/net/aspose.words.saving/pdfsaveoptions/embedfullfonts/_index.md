---
title: PdfSaveOptions.EmbedFullFonts
second_title: Справочник по API Aspose.Words для .NET
description: PdfSaveOptions свойство. Управляет тем как шрифты внедряются в результирующие PDFдокументы.
type: docs
weight: 120
url: /ru/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Управляет тем, как шрифты внедряются в результирующие PDF-документы.

```csharp
public bool EmbedFullFonts { get; set; }
```

### Примечания

Значение по умолчанию:`ЛОЖЬ`, что означает, что перед внедрением шрифты разделяются на поднаборы. Поднабор полезен, если вы хотите уменьшить размер выходного файла. Поднастройка удаляет из шрифта все неиспользуемые глифы .

Когда это значение установлено на`истинный`, полный файл шрифта встраивается в PDF без поднастройки . Это приведет к увеличению размера выходных файлов, но может оказаться полезным, если вы хотите отредактировать полученный PDF-файл позже (например, добавить больше текста).

Некоторые шрифты имеют большой размер (несколько мегабайт), и встраивание их без subsetting приведет к получению больших выходных документов.

### Примеры

Показывает, как включить или отключить поднабор при встраивании шрифтов во время рендеринга документа в PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Настройте источники шрифтов, чтобы гарантировать доступ к обоим шрифтам в этом документе.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Поскольку наш документ содержит собственный шрифт, его встраивание в выходной документ может оказаться желательным.
// Установите для свойства «EmbedFullFonts» значение «true», чтобы встроить каждый глиф каждого встроенного шрифта в выходной PDF-файл.
// Размер документа может стать очень большим, но при редактировании PDF мы сможем полностью использовать все шрифты.
// Установите для свойства "EmbedFullFonts" значение "false", чтобы применить поднабор к шрифтам, сохраняя только глифы
// который использует документ. Файл будет значительно меньше,
// но нам может понадобиться доступ к любым пользовательским шрифтам, если мы будем редактировать документ.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// Восстанавливаем исходные источники шрифтов.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../pdfsaveoptions/)
* сборка [Aspose.Words](../../../)


