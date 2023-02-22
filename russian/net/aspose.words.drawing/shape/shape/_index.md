---
title: Shape.Shape
second_title: Справочник по API Aspose.Words для .NET
description: Shape строитель. Создает новый объект формы.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Создает новый объект формы.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| shapeType | ShapeType | Тип создаваемой фигуры. |

### Примечания

Вы должны указать желаемые свойства формы после того, как вы создали фигуру.

### Примеры

Показывает, как вставить фигуру с изображением из локальной файловой системы в документ.

```csharp
Document doc = new Document();

// Открытый конструктор класса "Shape" создаст фигуру с типом разметки "ShapeMarkupLanguage.Vml".
// Если вам нужно создать фигуру не примитивного типа, например SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
// используйте DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Показывает, как создать и отформатировать текстовое поле.

```csharp
Document doc = new Document();

// Создаем плавающее текстовое поле.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Установить горизонтальное и вертикальное выравнивание текста внутри фигуры.
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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


