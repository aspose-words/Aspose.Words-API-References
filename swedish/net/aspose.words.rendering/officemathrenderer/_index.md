---
title: OfficeMathRenderer Class
linktitle: OfficeMathRenderer
articleTitle: OfficeMathRenderer
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Rendering.OfficeMathRenderer för att enkelt konvertera OfficeMath till fantastiska raster- eller vektorbilder för dina projekt.
type: docs
weight: 5290
url: /sv/net/aspose.words.rendering/officemathrenderer/
---
## OfficeMathRenderer class

Tillhandahåller metoder för att rendera en individ[`OfficeMath`](../../aspose.words.math/officemath/) till en raster- eller vektorbild eller till ett grafikobjekt.

För att lära dig mer, besök[Arbeta med OfficeMath](https://docs.aspose.com/words/net/working-with-officemath/) dokumentationsartikel.

```csharp
public class OfficeMathRenderer : NodeRendererBase
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OfficeMathRenderer](officemathrenderer/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Initierar en ny instans av den här klassen. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Hämtar formens faktiska gränser i punkter. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Hämtar formens ogenomskinliga gränser i punkter. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Hämtar formens faktiska storlek i punkter. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float*) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/)(*float, float, float*) | Beräknar formens gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float*) | Beräknar formens ogenomskinliga gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/)(*float, float, float*) | Beräknar formens ogenomskinliga gränser i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float*) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/)(*float, float, float*) | Beräknar formens storlek i pixlar för en angiven zoomfaktor och upplösning. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Återger formen till enGraphics objekt till en specificerad skala. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Återger formen till enGraphics objekt till en angiven storlek. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renderar formen till en bild och sparar i en ström. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Renderar formen till en SVG-bild och sparar i en dataström. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Renderar formen till en bild och sparar den i en fil. |
| [Save](../../aspose.words.rendering/noderendererbase/save/)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Återger formen till en SVG-bild och sparar den i en fil. |

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

* class [NodeRendererBase](../noderendererbase/)
* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
