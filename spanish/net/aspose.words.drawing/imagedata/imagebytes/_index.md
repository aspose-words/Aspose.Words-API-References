---
title: ImageData.ImageBytes
second_title: Referencia de API de Aspose.Words para .NET
description: ImageData propiedad. Obtiene o establece los bytes sin formato de la imagen almacenada en la forma.
type: docs
weight: 120
url: /es/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Obtiene o establece los bytes sin formato de la imagen almacenada en la forma.

```csharp
public byte[] ImageBytes { get; set; }
```

### Observaciones

Establecer el valor en`nulo` o una matriz vacía eliminará la imagen de la forma.

Devoluciones`nulo` si la imagen no está almacenada en el documento (por ejemplo, en este caso la imagen probablemente esté vinculada).

### Ejemplos

Muestra cómo crear un archivo de imagen a partir de los datos de imagen sin procesar de una forma.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() devuelve la matriz almacenada en la propiedad ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Guarde los datos de la imagen de la forma en un archivo de imagen en el sistema de archivos local.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../imagedata/)
* asamblea [Aspose.Words](../../../)


