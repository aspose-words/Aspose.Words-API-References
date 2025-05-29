---
title: ShapeBase.Right
linktitle: Right
articleTitle: Right
second_title: Aspose.Words för .NET
description: Upptäck ShapeBase Right-egenskapen för att enkelt komma åt den högra kantpositionen för din forms innehållsblock för exakt layoutkontroll.
type: docs
weight: 490
url: /sv/net/aspose.words.drawing/shapebase/right/
---
## ShapeBase.Right property

Hämtar positionen för den högra kanten av det block som innehåller formen.

```csharp
public double Right { get; }
```

## Anmärkningar

För en form på översta nivån är värdet i punkter och relativt till formankaret.

För former i en grupp finns värdet i koordinatrummet och enheterna för den överordnade gruppen.

## Exempel

Visar hur man infogar en flytande bild och anger dess position och storlek.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurera formens egenskap "RelativeHorizontalPosition" för att behandla värdet för egenskapen "Left"
 // som formens horisontella avstånd, i punkter, från sidans vänstra sida.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Ställ in formens horisontella avstånd från sidans vänstra sida till 100.
shape.Left = 100;

// Använd egenskapen "RelativeVerticalPosition" på ett liknande sätt för att placera formen 80 pt under sidans överkant.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Ställ in formens höjd, vilket automatiskt skalar bredden för att bevara måtten.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Egenskaperna "Nedre" och "Höger" innehåller bildens nedre och högra kanter.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
