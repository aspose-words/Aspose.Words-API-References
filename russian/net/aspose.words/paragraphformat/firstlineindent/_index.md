---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство FirstLineIndent объекта ParagraphFormat, чтобы легко настраивать отступы первой строки или висячие отступы в документах для улучшения их читаемости.
type: docs
weight: 120
url: /ru/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Возвращает или задает значение (в пунктах) для первой строки или висячего отступа.

Используйте положительные значения для установки отступа первой строки и отрицательные значения для установки отступа выступа.

```csharp
public double FirstLineIndent { get; set; }
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
