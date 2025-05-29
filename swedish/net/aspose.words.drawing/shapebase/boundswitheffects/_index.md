---
title: ShapeBase.BoundsWithEffects
linktitle: BoundsWithEffects
articleTitle: BoundsWithEffects
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase BoundsWithEffects för att få den slutliga omfattningen av din form efter att du har tillämpat riteffekter, mätt i punkter för precision.
type: docs
weight: 90
url: /sv/net/aspose.words.drawing/shapebase/boundswitheffects/
---
## ShapeBase.BoundsWithEffects property

Hämtar den slutliga utsträckningen som detta formobjekt har efter att riteffekter har tillämpats. Värdet mäts i punkter.

```csharp
public RectangleF BoundsWithEffects { get; }
```

## Exempel

Visar hur man kontrollerar hur en forms gränser påverkas av formeffekter.

```csharp
Document doc = new Document(MyDir + "Shape shadow effect.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// De två formerna är identiska vad gäller dimensioner och formtyp.
Assert.AreEqual(shapes[0].Width, shapes[1].Width);
Assert.AreEqual(shapes[0].Height, shapes[1].Height);
Assert.AreEqual(shapes[0].ShapeType, shapes[1].ShapeType);

// Den första formen har inga effekter, och den andra har en skugga och tjock kontur.
// Dessa effekter gör att den andra formens silhuett blir större än den första.
// Även om rektangelns storlek visas när vi klickar på dessa former i Microsoft Word,
// de synliga yttergränserna för den andra formen påverkas av skuggan och konturen och är därmed större.
// Vi kan använda metoden "AdjustWithEffects" för att se formens verkliga storlek.
Assert.AreEqual(0.0, shapes[0].StrokeWeight);
Assert.AreEqual(20.0, shapes[1].StrokeWeight);
Assert.False(shapes[0].ShadowEnabled);
Assert.True(shapes[1].ShadowEnabled);

Shape shape = shapes[0];

// Skapa ett RectangleF-objekt som representerar en rektangel,
// som vi potentiellt skulle kunna använda som koordinater och gränser för en form.
RectangleF rectangleF = new RectangleF(200, 200, 1000, 1000);

// Kör den här metoden för att justera rektangelns storlek för alla våra formeffekter.
RectangleF rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Eftersom formen inte har några kantförändrande effekter, påverkas inte dess kantdimensioner.
Assert.AreEqual(200, rectangleFOut.X);
Assert.AreEqual(200, rectangleFOut.Y);
Assert.AreEqual(1000, rectangleFOut.Width);
Assert.AreEqual(1000, rectangleFOut.Height);

// Verifiera den slutliga utsträckningen av den första formen, i punkter.
Assert.AreEqual(0, shape.BoundsWithEffects.X);
Assert.AreEqual(0, shape.BoundsWithEffects.Y);
Assert.AreEqual(147, shape.BoundsWithEffects.Width);
Assert.AreEqual(147, shape.BoundsWithEffects.Height);

shape = shapes[1];
rectangleF = new RectangleF(200, 200, 1000, 1000);
rectangleFOut = shape.AdjustWithEffects(rectangleF);

// Formeffekterna har flyttat det synliga övre vänstra hörnet av formen något.
Assert.AreEqual(171.5, rectangleFOut.X);
Assert.AreEqual(167, rectangleFOut.Y);

// Effekterna har också påverkat formens synliga dimensioner.
Assert.AreEqual(1045, rectangleFOut.Width);
Assert.AreEqual(1133.5, rectangleFOut.Height);

// Effekterna har också påverkat formens synliga gränser.
Assert.AreEqual(-28.5, shape.BoundsWithEffects.X);
Assert.AreEqual(-33, shape.BoundsWithEffects.Y);
Assert.AreEqual(192, shape.BoundsWithEffects.Width);
Assert.AreEqual(280.5, shape.BoundsWithEffects.Height);
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
