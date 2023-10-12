---
title: GraphicsQualityOptions.UseTileFlipMode
second_title: Aspose.Words per .NET API Reference
description: GraphicsQualityOptions proprietà. Ottiene o imposta un flag che indica se WrapMode è TileFlipXY.
type: docs
weight: 80
url: /it/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Ottiene o imposta un flag che indica se WrapMode è TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

### Osservazioni

ILWrapMode specifica come viene affiancata una texture o un gradiente quando è più piccolo dell'area da riempire.

Per impostazione predefinita utilizzaTile (specifica l'affiancamento senza capovolgimento). Ciò causa un rendering impreciso dell'immagine in scala (ad alta risoluzione).

Questa proprietà consente di passare a WrapModeTileFlipXY (specifica che le tessere vengono girate orizzontalmente mentre ti muovi lungo una riga e girate verticalmente mentre ti muovi lungo una colonna).

### Esempi

Mostra come evitare che appaia la linea bianca durante il rendering ad alta risoluzione.

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

### Guarda anche

* class [GraphicsQualityOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../graphicsqualityoptions/)
* assemblea [Aspose.Words](../../../)


