---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words для .NET
description: Узнайте, как свойство TextBox VerticalAnchor улучшает выравнивание текста внутри фигур, улучшая дизайн и читаемость ваших проектов.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Задает вертикальное выравнивание текста внутри фигуры.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Примечания

Значение по умолчанию:Top.

## Примеры

Показывает, как выровнять текстовое содержимое текстового поля по вертикали.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Установите свойство "VerticalAnchor" на "TextBoxAnchor.Top" для
// выровнять текст в этом текстовом поле по верхней стороне фигуры.
// Установите свойство "VerticalAnchor" на "TextBoxAnchor.Middle" для
// выровнять текст в этом текстовом поле по центру фигуры.
// Установите свойство "VerticalAnchor" на "TextBoxAnchor.Bottom" для
// выровнять текст в этом текстовом поле по нижнему краю фигуры.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Вертикальное выравнивание текста внутри текстовых полей доступно начиная с Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Смотрите также

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
