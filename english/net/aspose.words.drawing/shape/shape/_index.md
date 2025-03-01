---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words for .NET
description: Create unique shape objects effortlessly with our Shape Constructor. Design custom forms and enhance your projects with ease and precision!
type: docs
weight: 10
url: /net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Creates a new shape object.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | DocumentBase | The owner document. |
| shapeType | ShapeType | The type of the shape to create. |

## Remarks

You should specify desired shape properties after you created a shape.

## Examples

Shows how to insert a shape with an image from the local file system into a document.

```csharp
Document doc = new Document();

// The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.Vml" markup type.
// If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
// please use DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Shows how to create and format a text box.

```csharp
Document doc = new Document();

// Create a floating text box.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Set the horizontal, and vertical alignment of the text inside the shape.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Add a paragraph to the text box and add a run of text that the text box will display.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### See Also

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
