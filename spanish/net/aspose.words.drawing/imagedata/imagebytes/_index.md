---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageBytes de ImageData para administrar y manipular fácilmente bytes de imágenes sin procesar dentro de sus formas para obtener un contenido visual mejorado.
type: docs
weight: 120
url: /es/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Obtiene o establece los bytes sin procesar de la imagen almacenada en la forma.

```csharp
public byte[] ImageBytes { get; set; }
```

## Observaciones

Establecer el valor a`nulo` o una matriz vacía eliminará la imagen de la forma.

Devoluciones`nulo` Si la imagen no está almacenada en el documento (por ejemplo, la imagen probablemente esté vinculada en este caso).

## Ejemplos

Muestra cómo crear un archivo de imagen a partir de los datos de imagen sin procesar de una forma.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() devuelve la matriz almacenada en la propiedad ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Guarde los datos de imagen de la forma en un archivo de imagen en el sistema de archivos local.
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
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
