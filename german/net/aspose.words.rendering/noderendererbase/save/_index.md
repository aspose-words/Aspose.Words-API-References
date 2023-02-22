---
title: NodeRendererBase.Save
second_title: Aspose.Words für .NET-API-Referenz
description: NodeRendererBase methode. Rendert die Form in ein Bild und speichert sie in einer Datei.
type: docs
weight: 90
url: /de/net/aspose.words.rendering/noderendererbase/save/
---
## Save(string, ImageSaveOptions) {#save_1}

Rendert die Form in ein Bild und speichert sie in einer Datei.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Der Name für die Bilddatei. Wenn bereits eine Datei mit dem angegebenen Namen vorhanden ist, wird die vorhandene Datei überschrieben. |
| saveOptions | ImageSaveOptions | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann null sein. |

### Beispiele

Zeigt, wie ein Office Math-Objekt in eine Bilddatei im lokalen Dateisystem gerendert wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Erstellen Sie ein "ImageSaveOptions"-Objekt, das an die "Save"-Methode des Node-Renderers übergeben wird, um es zu ändern
// wie es den OfficeMath-Knoten in ein Bild rendert.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Setzen Sie die Eigenschaft "Scale" auf 5, um das Objekt auf das Fünffache seiner ursprünglichen Größe zu rendern.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Siehe auch

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../noderendererbase/)
* Montage [Aspose.Words](../../../)

---

## Save(Stream, ImageSaveOptions) {#save}

Rendert die Form in ein Bild und speichert sie in einem Stream.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, in dem das Bild der Form gespeichert werden soll. |
| saveOptions | ImageSaveOptions | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann null sein. Wenn dies null ist, wird das Bild im PNG-Format gespeichert. |

### Beispiele

Zeigt, wie Sie einen Form-Renderer verwenden, um Formen in Dateien im lokalen Dateisystem zu exportieren.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Das Dokument enthält 7 Formen, darunter eine Gruppenform mit 2 untergeordneten Formen.
// Wir rendern jede Form in eine Bilddatei im lokalen Dateisystem
// während die Gruppenformen ignoriert werden, da sie nicht erscheinen.
// Dies erzeugt 6 Bilddateien.
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
* namensraum [Aspose.Words.Rendering](../../noderendererbase/)
* Montage [Aspose.Words](../../../)


