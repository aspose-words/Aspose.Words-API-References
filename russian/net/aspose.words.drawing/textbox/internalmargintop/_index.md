---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextBox InternalMarginTop — управляйте верхним полем фигуры в пунктах для точной компоновки и повышения гибкости дизайна.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Указывает внутреннее верхнее поле в пунктах для фигуры.

```csharp
public double InternalMarginTop { get; set; }
```

## Примечания

Значение по умолчанию — 1/20 дюйма.

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
