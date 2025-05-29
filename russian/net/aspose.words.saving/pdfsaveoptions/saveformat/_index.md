---
title: PdfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PdfSaveOptions SaveFormat для легкого сохранения документов в формате PDF. Упростите управление файлами с помощью эффективных параметров сохранения.
type: docs
weight: 300
url: /ru/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть толькоPdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

### Смотрите также

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
