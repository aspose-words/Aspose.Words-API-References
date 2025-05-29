---
title: NodeRendererBase Class
linktitle: NodeRendererBase
articleTitle: NodeRendererBase
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Rendering.NodeRendererBase – din grund för effektiv Shape- och OfficeMath-rendering i dokumentbehandling.
type: docs
weight: 5280
url: /sv/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Basklass för[`ShapeRenderer`](../shaperenderer/) och[`OfficeMathRenderer`](../officemathrenderer/) .

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public abstract class NodeRendererBase
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Hämtar formens faktiska gränser i punkter. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Hämtar formens ogenomskinliga gränser i punkter. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Hämtar formens faktiska storlek i punkter. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(*float, float*) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(*float, float, float*) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(*float, float*) | Beräknar formens ogenomskinliga gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(*float, float, float*) | Beräknar formens ogenomskinliga gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(*float, float*) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Återger formen till enGraphics objekt till en specificerad skala. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Återger formen till enGraphics objekt till en angiven storlek. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renderar formen till en bild och sparar i en ström. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renderar formen till en SVG-bild och sparar i en dataström. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renderar formen till en bild och sparar den i en fil. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_3)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Återger formen till en SVG-bild och sparar den i en fil. |

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

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
