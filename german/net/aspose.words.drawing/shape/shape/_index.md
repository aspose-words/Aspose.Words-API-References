---
title: Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos einzigartige Formobjekte mit unserem Shape Constructor. Gestalten Sie individuelle Formulare und optimieren Sie Ihre Projekte mit Leichtigkeit und Präzision!
type: docs
weight: 10
url: /de/net/aspose.words.drawing/shape/shape/
---
## Shape constructor

Erstellt ein neues Formobjekt.

```csharp
public Shape(DocumentBase doc, ShapeType shapeType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| shapeType | ShapeType | Der Typ der zu erstellenden Form. |

## Bemerkungen

Sie sollten die gewünschten Formeigenschaften angeben, nachdem Sie eine Form erstellt haben.

## Beispiele

Zeigt, wie eine Form mit einem Bild aus dem lokalen Dateisystem in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();

// Der öffentliche Konstruktor der Klasse „Shape“ erstellt eine Form mit dem Markup-Typ „ShapeMarkupLanguage.Vml“.
// Wenn Sie eine Form eines nicht-primitiven Typs erstellen müssen, z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded oder DiagonalCornersRounded,
// bitte verwenden Sie DocumentBuilder.InsertShape.
Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.FromFile.docx");
```

Zeigt, wie ein Textfeld erstellt und formatiert wird.

```csharp
Document doc = new Document();

// Erstellen Sie ein schwebendes Textfeld.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Legen Sie die horizontale und vertikale Ausrichtung des Textes innerhalb der Form fest.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Fügen Sie dem Textfeld einen Absatz und einen Textlauf hinzu, der im Textfeld angezeigt wird.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [ShapeType](../../shapetype/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
