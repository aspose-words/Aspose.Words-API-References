---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words для .NET
description: Узнайте, как свойство CreateMissingOutlineLevels в OutlineOptions улучшает экспорт документов, автоматически создавая отсутствующие уровни структуры для лучшей организации.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Возвращает или задает значение, определяющее, следует ли создавать отсутствующие уровни структуры при экспорте документа .

Значение этого свойства по умолчанию:`ЛОЖЬ`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Примеры

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

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
