---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words per .NET
description: Scopri il metodo ShapeBase GetShapeRenderer per creare e riprodurre senza sforzo forme come immagini, migliorando con facilità i tuoi progetti di design.
type: docs
weight: 670
url: /it/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Crea e restituisce un oggetto che può essere utilizzato per trasformare questa forma in un'immagine.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Valore di ritorno

L'oggetto renderer per questa forma.

## Osservazioni

Questo metodo richiama semplicemente il[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) costruttore e passa questo oggetto come parametro.

## Esempi

Mostra come utilizzare uno shape renderer per esportare forme in file nel file system locale.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Nel documento sono presenti 7 forme, tra cui una forma di gruppo con 2 forme figlio.
// Renderizzeremo ogni forma in un file immagine nel file system locale
// ignorando le forme del gruppo poiché non hanno alcun aspetto.
// Verranno prodotti 6 file immagine.
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
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
