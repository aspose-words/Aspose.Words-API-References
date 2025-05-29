---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FitShapeToText в Microsoft Word автоматически подгоняет фигуры под ваш текст, улучшая презентацию документа.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Определяет, будет ли Microsoft Word увеличивать фигуру, чтобы вместить текст.

```csharp
public bool FitShapeToText { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как изменить размер текстового поля, чтобы оно полностью вмещало его содержимое.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Применяем эти значения к обоим членам, чтобы подогнать родительскую форму
// плотно обхватывает текстовое содержимое, игнорируя заданные нами размеры.
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
