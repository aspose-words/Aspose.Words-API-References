---
title: ParagraphFormat.AddSpaceBetweenFarEastAndAlpha
linktitle: AddSpaceBetweenFarEastAndAlpha
articleTitle: AddSpaceBetweenFarEastAndAlpha
second_title: Aspose.Words для .NET
description: Оптимизируйте внешний вид документа с помощью свойства ParagraphFormat AddSpaceBetweenFarEastAndAlpha, увеличивая интервал между латинским и восточноазиатским текстом.
type: docs
weight: 10
url: /ru/net/aspose.words/paragraphformat/addspacebetweenfareastandalpha/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndAlpha property

Возвращает или задает флаг, указывающий, регулируется ли автоматически межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце.

```csharp
public bool AddSpaceBetweenFarEastAndAlpha { get; set; }
```

## Примеры

Показывает, как вставить абзац в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// Метод Writeln завершает абзац после добавления текста
// а затем начинает новую строку, добавляя новый абзац.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
