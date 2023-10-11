---
title: GraphicsQualityOptions.UseTileFlipMode
second_title: Aspose.Words für .NET-API-Referenz
description: GraphicsQualityOptions eigendom. Ruft ein Flag ab oder setzt es das angibt ob WrapMode TileFlipXY ist.
type: docs
weight: 80
url: /de/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Ruft ein Flag ab oder setzt es, das angibt, ob WrapMode TileFlipXY ist.

```csharp
public bool UseTileFlipMode { get; set; }
```

### Bemerkungen

DerWrapMode Gibt an, wie eine Textur oder ein Farbverlauf gekachelt wird, wenn sie kleiner als der zu füllende Bereich ist.

Standardmäßig verwendetTile (gibt Kacheln ohne Spiegeln an). Dies führt zu einer ungenauen Darstellung des skalierten Bildes (mit hoher Auflösung).

Mit dieser Eigenschaft kann WrapMode auf umgeschaltet werdenTileFlipXY (Gibt an, dass Kacheln horizontal gespiegelt werden, wenn Sie sich entlang einer Zeile bewegen, und vertikal gespiegelt werden, wenn Sie sich entlang einer Spalte bewegen.)

### Beispiele

Zeigt, wie verhindert werden kann, dass beim Rendern mit hoher Auflösung eine weiße Linie erscheint.

```csharp
Document doc = new Document(MyDir + "Shape high dpi.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShapeRenderer renderer = shape.GetShapeRenderer();

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
{
    Resolution = 500, GraphicsQualityOptions = new GraphicsQualityOptions { UseTileFlipMode = true }
};
renderer.Save(ArtifactsDir + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
```

### Siehe auch

* class [GraphicsQualityOptions](../)
* namensraum [Aspose.Words.Saving](../../graphicsqualityoptions/)
* Montage [Aspose.Words](../../../)


