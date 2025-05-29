---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words para .NET
description: Descubra el método ShapeBase GetShapeRenderer para crear y renderizar sin esfuerzo formas como imágenes, mejorando sus proyectos de diseño con facilidad.
type: docs
weight: 670
url: /es/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Crea y devuelve un objeto que puede usarse para representar esta forma en una imagen.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Valor_devuelto

El objeto renderizador para esta forma.

## Observaciones

Este método simplemente invoca el[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) constructor y pasa este objeto como parámetro.

## Ejemplos

Muestra cómo utilizar un renderizador de formas para exportar formas a archivos en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Hay 7 formas en el documento, incluida una forma de grupo con 2 formas secundarias.
// Representaremos cada forma en un archivo de imagen en el sistema de archivos local
// mientras ignoramos las formas del grupo ya que no tienen apariencia.
// Esto producirá 6 archivos de imagen.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Ver también

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
