---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà UseTileFlipMode di GraphicsQualityOptions per controllare le impostazioni WrapMode e ottenere una qualità visiva migliorata nelle tue applicazioni.
type: docs
weight: 80
url: /it/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Ottiene o imposta un flag che indica se WrapMode è TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Osservazioni

ILWrapMode specifica come viene piastrellata una texture o un gradiente quando è più piccolo dell'area da riempire.

Per impostazione predefinita utilizzaTile (specifica l'affiancamento senza capovolgimento). Ciò causa un rendering impreciso dell'immagine ridimensionata (ad alta risoluzione).

Questa proprietà consente di cambiare WrapMode inTileFlipXY (specifica che le tessere vengono capovolte orizzontalmente quando ci si sposta lungo una riga e capovolte verticalmente quando ci si sposta lungo una colonna).

## Esempi

Mostra come evitare che venga visualizzata la linea bianca durante il rendering ad alta risoluzione.

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
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
