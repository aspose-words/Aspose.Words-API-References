---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase WrapType-egenskapen, styr inbäddade eller flytande former och anpassa textbrytning för ökad layoutflexibilitet.
type: docs
weight: 640
url: /sv/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

Definierar om formen är inbäddad eller flytande. För flytande former definieras radbrytningsläget för text runt formen.

```csharp
public WrapType WrapType { get; set; }
```

## Anmärkningar

Standardvärdet ärNone.

Har endast effekt för former på översta nivån.

## Exempel

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den mot sidans mitt.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
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

// Lägg till ett stycke i textrutan och lägg till en textsekvens som textrutan ska visa.
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

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
