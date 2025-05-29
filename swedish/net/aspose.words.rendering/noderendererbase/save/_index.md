---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: Upptäck NodeRendererBase Save-metoden. Rendera enkelt former som bilder och spara dem till filer för sömlös integration och förbättrad produktivitet.
type: docs
weight: 90
url: /sv/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

Renderar formen till en bild och sparar den i en fil.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på bildfilen. Om en fil med det angivna namnet redan finns, skrivs den befintliga filen över. |
| saveOptions | ImageSaveOptions | Anger alternativen som styr hur formen renderas och sparas. Kan vara`null`. |

## Exempel

Visar hur man renderar ett Office Math-objekt till en bildfil i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Skapa ett "ImageSaveOptions"-objekt för att skicka till nodrenderarens "Save"-metod för att modifiera
// hur den renderar OfficeMath-noden till en bild.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Sätt egenskapen "Scale" till 5 för att rendera objektet till fem gånger sin ursprungliga storlek.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

Återger formen till en SVG-bild och sparar den i en fil.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Namnet på bildfilen. Om en fil med det angivna namnet redan finns, skrivs den befintliga filen över. |
| saveOptions | SvgSaveOptions | Anger alternativen som styr hur formen renderas och sparas. Kan vara`null`. |

## Exempel

Visar hur man skickar spara-alternativ vid rendering av Office-matematik.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Se även

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Renderar formen till en bild och sparar i en ström.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Flödet där bilden av formen ska sparas. |
| saveOptions | ImageSaveOptions | Anger alternativen som styr hur formen renderas och sparas. Kan vara`null` . Om detta är`null`bilden kommer att sparas i PNG-format. |

## Exempel

Visar hur man använder en formrendering för att exportera former till filer i det lokala filsystemet.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Det finns 7 former i dokumentet, inklusive en gruppform med 2 underformer.
// Vi kommer att rendera varje form till en bildfil i det lokala filsystemet
// samtidigt som gruppformerna ignoreras eftersom de inte har något utseende.
// Detta kommer att producera 6 bildfiler.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

Renderar formen till en SVG-bild och sparar i en dataström.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen där SVG-bilden av formen ska sparas. |
| saveOptions | SvgSaveOptions | Anger alternativen som styr hur formen renderas och sparas. Kan vara`null` . Om detta är`null`, kommer bilden att sparas med standardinställningarna. |

## Exempel

Visar hur man skickar spara-alternativ vid rendering av Office-matematik.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Se även

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
