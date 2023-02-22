---
title: TextBox.InternalMarginRight
second_title: Справочник по API Aspose.Words для .NET
description: TextBox свойство. Указывает внутреннее правое поле в пунктах для фигуры.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

Указывает внутреннее правое поле в пунктах для фигуры.

```csharp
public double InternalMarginRight { get; set; }
```

### Примечания

Значение по умолчанию — 1/10 дюйма.

### Примеры

Показывает, как установить внутренние поля для текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить другое текстовое поле с определенными полями.
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
* пространство имен [Aspose.Words.Drawing](../../textbox/)
* сборка [Aspose.Words](../../../)


