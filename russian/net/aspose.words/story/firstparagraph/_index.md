---
title: Story.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Story FirstParagraph, которое позволяет легко извлекать первый абзац любой истории, улучшая ваш контент и взаимодействие с пользователями.
type: docs
weight: 10
url: /ru/net/aspose.words/story/firstparagraph/
---
## Story.FirstParagraph property

Получает первый абзац в истории.

```csharp
public Paragraph FirstParagraph { get; }
```

## Примеры

Показывает, как отформатировать фрагмент текста, используя его свойство шрифта.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
