---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words для .NET
description: Извлеките первый абзац фигуры без усилий. Улучшите макет вашего документа с помощью нашей простой в использовании функции Shape FirstParagraph.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Получает первый абзац в форме.

```csharp
public Paragraph FirstParagraph { get; }
```

## Примеры

Показывает, как создать и отформатировать текстовое поле.

```csharp
Document doc = new Document();

// Создаем плавающее текстовое поле.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Устанавливаем горизонтальное и вертикальное выравнивание текста внутри фигуры.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Добавьте абзац в текстовое поле и добавьте фрагмент текста, который будет отображаться в текстовом поле.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Смотрите также

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
