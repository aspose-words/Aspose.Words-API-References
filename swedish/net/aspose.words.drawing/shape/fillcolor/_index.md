---
title: Shape.FillColor
linktitle: FillColor
articleTitle: FillColor
second_title: Aspose.Words för .NET
description: Shape FillColor fast egendom. Definierar penselfärgen som fyller den stängda banan för formen i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/shape/fillcolor/
---
## Shape.FillColor property

Definierar penselfärgen som fyller den stängda banan för formen.

```csharp
public Color FillColor { get; set; }
```

## Anmärkningar

Detta är en genväg till[`Color`](../../fill/color/) fast egendom.

Standardvärdet är White.

## Exempel

Visar hur man fyller en form med enfärgad.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skriv lite text och täck den sedan med en flytande form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Använd egenskapen "StrokeColor" för att ställa in färgen på formens kontur.
shape.StrokeColor = Color.CadetBlue;

// Använd egenskapen "FillColor" för att ställa in färgen på formens insida.
shape.FillColor = Color.LightBlue;

// Egenskapen "Opacity" bestämmer hur transparent färgen är på en skala 0-1,
// där 1 är helt ogenomskinlig och 0 är osynlig.
// Formfyllningen är som standard helt ogenomskinlig, så vi kan inte se texten som denna form är ovanpå.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Ställ in formfyllningsfärgens opacitet till ett lägre värde så att vi kan se texten under den.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### Se även

* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
