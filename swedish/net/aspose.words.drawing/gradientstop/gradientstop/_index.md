---
title: GradientStop
linktitle: GradientStop
articleTitle: GradientStop
second_title: Aspose.Words för .NET
description: GradientStop byggare. Initierar en ny instans avGradientStop class i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/gradientstop/gradientstop/
---
## GradientStop(*Color, double*) {#constructor}

Initierar en ny instans av[`GradientStop`](../) class.

```csharp
public GradientStop(Color color, double position)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| color | Color | Representerar färgen på gradientstoppet. |
| position | Double | Representerar positionen för ett stopp inom gradienten uttryckt som en procent i intervallet 0,0 till 1,0. |

## Exempel

Visar hur man lägger till övertoningsstopp i övertoningsfyllningen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Få gradient stoppar samling.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Ändra första gradientstopp.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Lägg till nytt övertoningsstopp i slutet av samlingen.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Ta bort gradientstopp vid index 1.
gradientStops.RemoveAt(1);
// Och infoga nytt gradientstopp vid samma index 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Ta bort sista gradientstopp i samlingen.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Använd efterlevnadsalternativet för att definiera formen med DML
// om du vill få egenskapen "GradientStops" efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Se även

* class [GradientStop](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## GradientStop(*Color, double, double*) {#constructor_1}

Initierar en ny instans av[`GradientStop`](../) class.

```csharp
public GradientStop(Color color, double position, double transparency)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| color | Color | Representerar färgen på gradientstoppet. |
| position | Double | Representerar positionen för ett stopp inom gradienten uttryckt som en procent i intervallet 0,0 till 1,0. |
| transparency | Double | Representerar genomskinligheten för ett stopp inom gradienten uttryckt som en procent i intervallet 0,0 till 1,0. |

## Exempel

Visar hur man lägger till övertoningsstopp i övertoningsfyllningen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
shape.Fill.TwoColorGradient(Color.Green, Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2);

// Få gradient stoppar samling.
GradientStopCollection gradientStops = shape.Fill.GradientStops;

// Ändra första gradientstopp.            
gradientStops[0].Color = Color.Aqua;            
gradientStops[0].Position = 0.1;
gradientStops[0].Transparency = 0.25;

// Lägg till nytt övertoningsstopp i slutet av samlingen.
GradientStop gradientStop = new GradientStop(Color.Brown, 0.5);
gradientStops.Add(gradientStop);

// Ta bort gradientstopp vid index 1.
gradientStops.RemoveAt(1);
// Och infoga nytt gradientstopp vid samma index 1.
gradientStops.Insert(1, new GradientStop(Color.Chocolate, 0.75, 0.3));

// Ta bort sista gradientstopp i samlingen.
gradientStop = gradientStops[2];
gradientStops.Remove(gradientStop);

Assert.AreEqual(2, gradientStops.Count);

Assert.AreEqual(Color.FromArgb(255, 0, 255, 255), gradientStops[0].BaseColor);
Assert.AreEqual(Color.Aqua.ToArgb(), gradientStops[0].Color.ToArgb());
Assert.AreEqual(0.1d, gradientStops[0].Position, 0.01d);
Assert.AreEqual(0.25d, gradientStops[0].Transparency, 0.01d);

Assert.AreEqual(Color.Chocolate.ToArgb(), gradientStops[1].Color.ToArgb());
Assert.AreEqual(0.75d, gradientStops[1].Position, 0.01d);
Assert.AreEqual(0.3d, gradientStops[1].Transparency, 0.01d);

// Använd efterlevnadsalternativet för att definiera formen med DML
// om du vill få egenskapen "GradientStops" efter att dokumentet har sparats.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientStops.docx", saveOptions);
```

### Se även

* class [GradientStop](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
