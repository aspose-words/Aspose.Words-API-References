---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words para .NET
description: ImageData ToStream método. Crea y devuelve una secuencia que contiene los bytes de la imagen en C#.
type: docs
weight: 230
url: /es/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Crea y devuelve una secuencia que contiene los bytes de la imagen.

```csharp
public Stream ToStream()
```

## Observaciones

Si los bytes de la imagen se almacenan en la forma, crea y devuelve unMemoryStream objeto.

Si la imagen está vinculada y almacenada en un archivo, abre el archivo y devuelve unFileStream objeto.

Si la imagen está vinculada y almacenada en una URL externa, descarga el archivo y devuelve unMemoryStream objeto.

¿Es responsabilidad de la persona que llama deshacerse del objeto de flujo?

## Ejemplos

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
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
