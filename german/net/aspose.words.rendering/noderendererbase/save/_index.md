---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words für .NET
description: Entdecken Sie die NodeRendererBase-Speichermethode. Rendern Sie Formen einfach als Bilder und speichern Sie sie in Dateien für eine nahtlose Integration und gesteigerte Produktivität.
type: docs
weight: 90
url: /de/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

Rendert die Form in ein Bild und speichert sie in einer Datei.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name der Bilddatei. Wenn bereits eine Datei mit dem angegebenen Namen vorhanden ist, wird die vorhandene Datei überschrieben. |
| saveOptions | ImageSaveOptions | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann sein`null`. |

## Beispiele

Zeigt, wie ein Office Math-Objekt in eine Bilddatei im lokalen Dateisystem gerendert wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das Sie an die "Save"-Methode des Knoten-Renderers übergeben, um es zu ändern
// wie es den OfficeMath-Knoten in ein Bild rendert.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft „Scale“ auf 5, um das Objekt auf das Fünffache seiner Originalgröße zu rendern.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

Rendert die Form in ein SVG-Bild und speichert sie in einer Datei.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name der Bilddatei. Wenn bereits eine Datei mit dem angegebenen Namen vorhanden ist, wird die vorhandene Datei überschrieben. |
| saveOptions | SvgSaveOptions | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann sein`null`. |

## Beispiele

Zeigt, wie beim Rendern von Office-Mathematik Speicheroptionen übergeben werden.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Siehe auch

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Rendert die Form in ein Bild und speichert sie in einem Stream.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, in dem das Bild der Form gespeichert werden soll. |
| saveOptions | ImageSaveOptions | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann sein`null` . Wenn dies`null`das Bild wird im PNG-Format gespeichert. |

## Beispiele

Zeigt, wie Sie mit einem Formrenderer Formen in Dateien im lokalen Dateisystem exportieren.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Das Dokument enthält 7 Formen, darunter eine Gruppenform mit 2 untergeordneten Formen.
// Wir rendern jede Form in eine Bilddatei im lokalen Dateisystem
// wobei die Gruppenformen ignoriert werden, da sie nicht angezeigt werden.
// Dadurch werden 6 Bilddateien erstellt.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

Rendert die Form in ein SVG-Bild und speichert sie in einem Stream.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, in dem das SVG-Bild der Form gespeichert werden soll. |
| saveOptions | SvgSaveOptions | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann sein`null` . Wenn dies`null`, wird das Bild mit den Standardoptionen gespeichert. |

## Beispiele

Zeigt, wie beim Rendern von Office-Mathematik Speicheroptionen übergeben werden.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Siehe auch

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
