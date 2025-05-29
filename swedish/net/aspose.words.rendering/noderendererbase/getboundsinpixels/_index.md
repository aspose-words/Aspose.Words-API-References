---
title: NodeRendererBase.GetBoundsInPixels
linktitle: GetBoundsInPixels
articleTitle: GetBoundsInPixels
second_title: Aspose.Words för .NET
description: Upptäck NodeRendererBase GetBoundsInPixels-metoden för att exakt beräkna formens dimensioner i pixlar baserat på zoom och upplösning för förbättrad precision.
type: docs
weight: 40
url: /sv/net/aspose.words.rendering/noderendererbase/getboundsinpixels/
---
## GetBoundsInPixels(*float, float*) {#getboundsinpixels}

Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning.

```csharp
public Rectangle GetBoundsInPixels(float scale, float dpi)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| scale | Single | Zoomfaktorn (1,0 är 100 %). |
| dpi | Single | Upplösningen (horisontell och vertikal) som ska konverteras från punkter till pixlar (punkter per tum). |

### Returvärde

Den faktiska (som den återges på sidan) avgränsningsramen för formen i pixlar.

## Anmärkningar

Den här metoden konverterar[`BoundsInPoints`](../boundsinpoints/) till en rektangel i pixlar.

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

* class [NodeRendererBase](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)

---

## GetBoundsInPixels(*float, float, float*) {#getboundsinpixels_1}

Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning.

```csharp
public Rectangle GetBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| scale | Single | Zoomfaktorn (1,0 är 100 %). |
| horizontalDpi | Single | Den horisontella upplösningen som ska konverteras från punkter till pixlar (punkter per tum). |
| verticalDpi | Single | Den vertikala upplösningen som ska konverteras från punkter till pixlar (punkter per tum). |

### Returvärde

Den faktiska (som den återges på sidan) avgränsningsramen för formen i pixlar.

## Anmärkningar

Den här metoden konverterar[`BoundsInPoints`](../boundsinpoints/) till en rektangel i pixlar.

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

* class [NodeRendererBase](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
