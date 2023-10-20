---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words для .NET
description: ShapeBase WrapType свойство. Определяет является ли фигура строковой или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры на С#.
type: docs
weight: 600
url: /ru/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

Определяет, является ли фигура строковой или плавающей. Для плавающих фигур определяет режим обтекания текста вокруг фигуры.

```csharp
public WrapType WrapType { get; set; }
```

## Примечания

Значение по умолчанию:None.

Имеет эффект только для фигур верхнего уровня.

## Примеры

Показывает, как вставить плавающее изображение в центр страницы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем плавающее изображение, которое появится за перекрывающимся текстом, и выравниваем его по центру страницы.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Показывает, как создать и отформатировать текстовое поле.

```csharp
Document doc = new Document();

// Создаём плавающее текстовое поле.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Устанавливаем горизонтальное и вертикальное выравнивание текста внутри фигуры.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Добавляем абзац в текстовое поле и добавляем текст, который будет отображаться в текстовом поле.
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

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
