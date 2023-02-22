---
title: ImageData.ImageType
second_title: Referencia de API de Aspose.Words para .NET
description: ImageData propiedad. Obtiene el tipo de imagen.
type: docs
weight: 140
url: /es/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Obtiene el tipo de imagen.

```csharp
public ImageType ImageType { get; }
```

### Ejemplos

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
        // Podemos determinar una extensión de archivo para cada imagen automáticamente, en función de su formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Ver también

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../imagedata/)
* asamblea [Aspose.Words](../../../)


