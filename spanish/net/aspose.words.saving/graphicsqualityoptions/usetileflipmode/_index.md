---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words para .NET
description: GraphicsQualityOptions UseTileFlipMode propiedad. Obtiene o establece un indicador que indica si WrapMode es TileFlipXY en C#.
type: docs
weight: 80
url: /es/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Obtiene o establece un indicador que indica si WrapMode es TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Observaciones

ElWrapMode especifica cómo se mosaico una textura o un degradado cuando es menor que el área que se está rellenando.

Por defecto utilizaTile (especifica mosaico sin voltear). Esto provoca una representación inexacta de la imagen escalada (con alta resolución).

Esta propiedad permite cambiar WrapMode aTileFlipXY (especifica que los mosaicos se voltean horizontalmente a medida que se mueve a lo largo de una fila y se voltean verticalmente a medida que se mueve a lo largo de una columna).

## Ejemplos

Muestra cómo evitar que aparezca la línea blanca al renderizar con alta resolución.

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

### Ver también

* class [GraphicsQualityOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
