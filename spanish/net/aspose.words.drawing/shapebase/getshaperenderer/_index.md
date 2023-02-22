---
title: ShapeBase.GetShapeRenderer
second_title: Referencia de API de Aspose.Words para .NET
description: ShapeBase método. Crea y devuelve un objeto que se puede usar para convertir esta forma en una imagen.
type: docs
weight: 600
url: /es/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Crea y devuelve un objeto que se puede usar para convertir esta forma en una imagen.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Valor_devuelto

El objeto renderizador para esta forma.

### Observaciones

Este método simplemente invoca el[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) constructor y pasa este objeto como parámetro.

### Ejemplos

Muestra cómo usar un renderizador de formas para exportar formas a archivos en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Hay 7 formas en el documento, incluida una forma de grupo con 2 formas secundarias.
// Representaremos cada forma en un archivo de imagen en el sistema de archivos local
// mientras ignora las formas del grupo ya que no tienen apariencia.
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
* espacio de nombres [Aspose.Words.Drawing](../../shapebase/)
* asamblea [Aspose.Words](../../../)


