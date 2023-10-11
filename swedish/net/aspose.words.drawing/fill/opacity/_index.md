---
title: Fill.Opacity
second_title: Aspose.Words för .NET API Referens
description: Fill fast egendom. Hämtar eller ställer in graden av opacitet för den angivna fyllningen som ett värde mellan 00 clear och 10 opak.
type: docs
weight: 150
url: /sv/net/aspose.words.drawing/fill/opacity/
---
## Fill.Opacity property

Hämtar eller ställer in graden av opacitet för den angivna fyllningen som ett värde mellan 0,0 (clear) och 1,0 (opak).

```csharp
public double Opacity { get; set; }
```

### Anmärkningar

Denna egenskap är motsatsen till egendom[`Transparency`](../transparency/).

### Exempel

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

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../fill/)
* hopsättning [Aspose.Words](../../../)


