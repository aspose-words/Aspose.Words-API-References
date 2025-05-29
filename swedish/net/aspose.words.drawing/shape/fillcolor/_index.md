---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Formfyllnadsfärg för att anpassa dina designer med livfulla penselfärger som framhäver dina former och lyfter dina projekt.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Definierar penselfärgen som fyller formens slutna bana.

```csharp
public Color FillColor { get; set; }
```

## Anmärkningar

Detta är en genväg till[`Color`](../../fill/color/) egendom.

Standardvärdet är White .

## Exempel

Visar hur man fyller en form med en helfärg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skriv lite text och täck den sedan med en flytande form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Använd egenskapen "StrokeColor" för att ange färgen på formens kontur.
shape.StrokeColor = Color.CadetBlue;

// Använd egenskapen "FillColor" för att ange färgen på formens insida.
shape.FillColor = Color.LightBlue;

// Egenskapen "Opacitet" avgör hur transparent färgen är på en skala från 0 till 1,
// där 1 är helt ogenomskinlig och 0 är osynlig.
// Formfyllningen är som standard helt ogenomskinlig, så vi kan inte se texten som formen ligger ovanpå.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Ställ in fyllningsfärgens opacitet till ett lägre värde så att vi kan se texten under den.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Se även

* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
