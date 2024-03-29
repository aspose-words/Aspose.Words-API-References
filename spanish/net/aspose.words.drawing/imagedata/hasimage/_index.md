---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words para .NET
description: ImageData HasImage propiedad. Devolucionesverdadero si la forma tiene bytes de imagen o vincula una imagen en C#.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Devoluciones`verdadero` si la forma tiene bytes de imagen o vincula una imagen.

```csharp
public bool HasImage { get; }
```

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
