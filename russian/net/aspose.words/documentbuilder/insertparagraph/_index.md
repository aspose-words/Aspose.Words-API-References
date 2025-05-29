---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words для .NET
description: Улучшайте свои документы без особых усилий с помощью метода InsertParagraph в DocumentBuilder, позволяющего плавно разбивать абзацы для улучшения читаемости.
type: docs
weight: 450
url: /ru/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Вставляет разрыв абзаца в документ.

```csharp
public Paragraph InsertParagraph()
```

### Возвращаемое значение

Узел абзаца, который был только что вставлен. Это тот же узел, что и[`CurrentParagraph`](../currentparagraph/).

## Примечания

Текущее форматирование абзаца, заданное[`ParagraphFormat`](../paragraphformat/) используется имущество.

Разбивает текущий абзац на два. После вставки абзаца курсор помещается в начало нового абзаца.

Исключение возникает, если в текущей позиции курсора невозможно вставить разрыв абзаца.

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

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
