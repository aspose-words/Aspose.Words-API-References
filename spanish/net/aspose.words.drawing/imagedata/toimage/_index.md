---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words para .NET
description: ImageData ToImage método. Obtiene la imagen almacenada en la forma comoImage objeto en C#.
type: docs
weight: 220
url: /es/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Obtiene la imagen almacenada en la forma comoImage objeto.

```csharp
public Image ToImage()
```

## Observaciones

un nuevoImage El objeto se crea cada vez que se llama a este método.

Es responsabilidad de la persona que llama disponer del objeto de imagen.

## Ejemplos

Muestra cómo guardar todas las imágenes de un documento en el sistema de archivos.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Las formas con el conjunto de indicadores "HasImage" almacenan y muestran todas las imágenes del documento.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Revisa cada forma y guarda su imagen.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
