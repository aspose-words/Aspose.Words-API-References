---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words для .NET
description: TextBox FitShapeToText свойство. Определяет будет ли Microsoft Word увеличивать форму до размера текста на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Определяет, будет ли Microsoft Word увеличивать форму до размера текста.

```csharp
public bool FitShapeToText { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как изменить размер текстового поля, чтобы оно плотно вписывалось в его содержимое.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Применяем эти значения к обоим элементам, чтобы родительская фигура соответствовала размеру
// плотно окружает текстовое содержимое, игнорируя установленные нами размеры.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Смотрите также

* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
