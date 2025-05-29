---
title: FileFormatUtil.ImageTypeToExtension
linktitle: ImageTypeToExtension
articleTitle: ImageTypeToExtension
second_title: Aspose.Words para .NET
description: Convierte fácilmente los tipos de imagen de Aspose.Words a extensiones de archivo con el método FileFormatUtil. ¡Obtén extensiones precisas en minúsculas en segundos!
type: docs
weight: 50
url: /es/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Convierte un valor enumerado de tipo de imagen Aspose.Words en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | Se lanza cuando no se puede convertir. |

## Ejemplos

Muestra cómo extraer imágenes de un documento y guardarlas en el sistema de archivos local como archivos individuales.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Obtener la colección de formas del documento,
// y guarde los datos de imagen de cada forma con una imagen como un archivo en el sistema de archivos local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Los datos de imagen de las formas pueden contener imágenes de muchos formatos de imagen posibles.
        //Podemos determinar automáticamente una extensión de archivo para cada imagen, en función de su formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Ver también

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
