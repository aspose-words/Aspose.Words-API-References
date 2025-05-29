---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words para .NET
description: Descubra si una forma es una imagen con la propiedad IsImage de ShapeBase. Identifique fácilmente las formas de las imágenes para mejorar la flexibilidad y la funcionalidad del diseño.
type: docs
weight: 300
url: /es/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Devuelve`verdadero` Si esta forma es una forma de imagen.

```csharp
public bool IsImage { get; }
```

## Ejemplos

Muestra cómo abrir un documento HTML con imágenes desde una transmisión usando una URI base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pasar la URI de la carpeta base mientras se carga
    // para que se puedan encontrar todas las imágenes con URI relativas en el documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifique que la primera forma del documento contenga una imagen válida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
