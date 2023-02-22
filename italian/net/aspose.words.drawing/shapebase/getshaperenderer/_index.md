---
title: ShapeBase.GetShapeRenderer
second_title: Aspose.Words per .NET API Reference
description: ShapeBase metodo. Crea e restituisce un oggetto che può essere utilizzato per rendere questa forma in unimmagine.
type: docs
weight: 600
url: /it/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Crea e restituisce un oggetto che può essere utilizzato per rendere questa forma in un'immagine.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Valore di ritorno

L'oggetto renderer per questa forma.

### Osservazioni

Questo metodo invoca semplicemente il[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) costruttore e passa questo oggetto come parametro.

### Esempi

Mostra come utilizzare un renderer di forme per esportare forme in file nel file system locale.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Ci sono 7 forme nel documento, inclusa una forma di gruppo con 2 forme figlio.
// Rendering di ogni forma in un file immagine nel file system locale
// ignorando le forme di gruppo poiché non hanno aspetto.
// Questo produrrà 6 file immagine.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Guarda anche

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


