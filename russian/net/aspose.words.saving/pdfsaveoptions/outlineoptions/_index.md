---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OutlineOptions PdfSaveOptions, чтобы без труда настраивать контуры PDF-файлов. Улучшите навигацию и улучшите удобство использования документа!
type: docs
weight: 240
url: /ru/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Позволяет указать параметры контура.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Примечания

Контуры можно создавать из заголовков и закладок.

Для заголовков уровень структуры определяется уровнем заголовка.

Можно установить максимальный уровень заголовков, включаемых в контуры, или вообще отключить контуры заголовков.

Для закладок уровень структуры может быть установлен в параметрах как значение по умолчанию для всех закладок или как индивидуальные значения для определенных закладок.

Кроме того, контуры можно экспортировать в формат XPS, используя ту же программу`OutlineOptions` сорт.

## Примеры

Показывает, как ограничить уровень заголовков, которые будут отображаться в структуре сохраненного PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки, которые могут служить записями оглавления уровней 1, 2 и 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "2", чтобы исключить из структуры все заголовки, уровни которых выше 2.
// Последние два заголовка, которые мы вставили выше, не появятся.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Показывает, как работать с уровнями структуры, не содержащими соответствующих заголовков, при сохранении PDF-документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки, которые могут служить записями оглавления уровней 1 и 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "5", чтобы включить в структуру все заголовки уровней 5 и ниже.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Этот документ содержит заголовки уровней 1 и 5 и не содержит заголовков уровней 2, 3 и 4.
// В выходном PDF-документе уровни структуры 2, 3 и 4 будут считаться «отсутствующими».
// Установите свойство "CreateMissingOutlineLevels" в значение "true", чтобы включить все отсутствующие уровни в контур,
// оставляем пустые записи структуры, так как нет пригодных для использования заголовков.
// Установите свойство "CreateMissingOutlineLevels" в значение "false", чтобы игнорировать отсутствующие уровни контура,
// и обрабатывать заголовки уровня 5 структуры как заголовки уровня 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Смотрите также

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
