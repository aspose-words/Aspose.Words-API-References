---
title: TextBox.InternalMarginLeft
linktitle: InternalMarginLeft
articleTitle: InternalMarginLeft
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextBox InternalMarginLeft, позволяющее настроить внутреннее левое поле фигуры в пунктах для повышения гибкости дизайна.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/textbox/internalmarginleft/
---
## TextBox.InternalMarginLeft property

Указывает внутреннее левое поле в пунктах для фигуры.

```csharp
public double InternalMarginLeft { get; set; }
```

## Примечания

Значение по умолчанию — 1/10 дюйма.

## Примеры

Показывает, как установить внутренние поля для текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте еще одно текстовое поле с определенными полями.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### Смотрите также

* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
