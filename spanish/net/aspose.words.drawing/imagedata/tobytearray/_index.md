---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words para .NET
description: Convierte cualquier imagen en una matriz de bytes fácilmente con el método ImageData ToByteArray. ¡Accede fácilmente a bytes de imágenes desde fuentes almacenadas o vinculadas!
type: docs
weight: 220
url: /es/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Devuelve bytes de imagen para cualquier imagen, independientemente de si la imagen está almacenada o vinculada.

```csharp
public byte[] ToByteArray()
```

## Observaciones

Si la imagen está vinculada, descarga la imagen cada vez que se llama.

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
