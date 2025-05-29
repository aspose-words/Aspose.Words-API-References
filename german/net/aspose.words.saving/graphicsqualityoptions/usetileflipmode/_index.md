---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die UseTileFlipMode-Eigenschaft von GraphicsQualityOptions, um die WrapMode-Einstellungen für eine verbesserte visuelle Qualität in Ihren Anwendungen zu steuern.
type: docs
weight: 80
url: /de/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Ruft ein Flag ab oder legt es fest, das angibt, ob WrapMode TileFlipXY ist.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Bemerkungen

DerWrapMode gibt an, wie eine Textur oder ein Farbverlauf gekachelt wird, wenn er kleiner ist als der zu füllende Bereich.

Standardmäßig verwendetTile (gibt Kacheln ohne Spiegeln an). Dies führt zu einer ungenauen Darstellung des skalierten Bildes (mit hoher Auflösung).

Mit dieser Eigenschaft können Sie den WrapMode umstellen aufTileFlipXY (gibt an, dass Kacheln horizontal gespiegelt werden, wenn Sie sich entlang einer Zeile bewegen, und vertikal, wenn Sie sich entlang einer Spalte bewegen).

## Beispiele

Zeigt, wie verhindert werden kann, dass beim Rendern mit hoher Auflösung die weiße Linie erscheint.

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
