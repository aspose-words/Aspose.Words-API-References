---
title: OfficeMathRenderer
linktitle: OfficeMathRenderer
articleTitle: OfficeMathRenderer
second_title: Aspose.Words för .NET
description: Skapa dynamiska matematiska presentationer enkelt med OfficeMathRenderer-konstruktorn. Förbättra dina dokument med sömlös matematisk rendering!
type: docs
weight: 10
url: /sv/net/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer constructor

Initierar en ny instans av den här klassen.

```csharp
public OfficeMathRenderer(OfficeMath math)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| math | OfficeMath | De[`OfficeMath`](../../../aspose.words.math/officemath/) objektet som du vill rendera. |

## Exempel

Visar hur man mäter och skalar former.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verifiera storleken på bilden som OfficeMath-objektet skapar när vi renderar den.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Former med genomskinliga delar kan innehålla olika värden i egenskaperna "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Hämta formstorleken i pixlar, med linjär skalning till en specifik DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Hämta formstorleken i pixlar, men med olika DPI för de horisontella och vertikala dimensionerna.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// De ogenomskinliga gränserna kan variera även här.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Se även

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [OfficeMathRenderer](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
