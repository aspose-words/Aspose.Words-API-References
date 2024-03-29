---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words för .NET
description: Shape byggare. Skapar ett nytt formobjekt i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Skapar ett nytt formobjekt.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| shapeType | ShapeType | Typen av formen som ska skapas. |

## Anmärkningar

Du bör ange önskade formegenskaper efter att du skapat en form.

## Exempel

Visar hur man infogar en form med en bild från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();

// "Shape"-klassens offentliga konstruktor kommer att skapa en form med "ShapeMarkupLanguage.Vml"-typ.
// Om du behöver skapa en form av en icke-primitiv typ, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded eller DiagonalCornersRounded,
// använd DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Visar hur man skapar och formaterar en textruta.

```csharp
Document doc = new Document();

// Skapa en flytande textruta.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Ställ in den horisontella och vertikala justeringen av texten inuti formen.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Lägg till ett stycke i textrutan och lägg till en serie text som textrutan kommer att visa.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Se även

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
