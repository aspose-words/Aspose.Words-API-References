---
title: DocumentBuilder.CurrentSection
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder fast egendom. Hämtar avsnittet som för närvarande är valt i dettaDocumentBuilder .
type: docs
weight: 60
url: /sv/net/aspose.words/documentbuilder/currentsection/
---
## DocumentBuilder.CurrentSection property

Hämtar avsnittet som för närvarande är valt i detta[`DocumentBuilder`](../) .

```csharp
public Section CurrentSection { get; }
```

### Exempel

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

* class [Section](../../section/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


