---
title: ShapeBase.Right
linktitle: Right
articleTitle: Right
second_title: Aspose.Words för .NET
description: ShapeBase Right fast egendom. Får positionen för den högra kanten av det innehållande blocket av formen i C#.
type: docs
weight: 460
url: /sv/net/aspose.words.drawing/shapebase/right/
---
## ShapeBase.Right property

Får positionen för den högra kanten av det innehållande blocket av formen.

```csharp
public double Right { get; }
```

## Anmärkningar

För en form på toppnivå är värdet i punkter och i förhållande till formankaret.

För former i en grupp finns värdet i koordinatutrymmet och enheterna för den överordnade gruppen.

## Exempel

Visar hur man infogar en flytande bild och anger dess position och storlek.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurera formens "RelativeHorizontalPosition"-egenskap för att behandla värdet på egenskapen "Left"
 // som formens horisontella avstånd, i punkter, från sidans vänstra sida.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Ställ in formens horisontella avstånd från sidans vänstra sida till 100.
shape.Left = 100;

// Använd egenskapen "RelativeVerticalPosition" på liknande sätt för att placera formen 80 pkt under toppen av sidan.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Ställ in formens höjd, vilket automatiskt skalar bredden för att bevara dimensionerna.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Egenskaperna "Bottom" och "Right" innehåller bildens nedre och högra kanter.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
