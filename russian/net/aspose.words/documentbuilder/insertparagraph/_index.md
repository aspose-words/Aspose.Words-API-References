---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words для .NET
description: DocumentBuilder InsertParagraph метод. Вставляет в документ разрыв абзаца на С#.
type: docs
weight: 420
url: /ru/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Вставляет в документ разрыв абзаца.

```csharp
public Paragraph InsertParagraph()
```

### Возвращаемое значение

Узел абзаца, который был только что вставлен. Это тот же узел, что и[`CurrentParagraph`](../currentparagraph/).

## Примечания

Текущее форматирование абзаца, заданное параметром[`ParagraphFormat`](../paragraphformat/) имущество используется.

Разбивает текущий абзац на две части. После вставки абзаца курсор помещается в начало нового абзаца.

Исключение выдается, если невозможно вставить разрыв абзаца в текущей позиции курсора.

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
// а затем начинается новая строка, добавляющая новый абзац.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Смотрите также

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
