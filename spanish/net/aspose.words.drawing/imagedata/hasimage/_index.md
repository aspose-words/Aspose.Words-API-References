---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageData HasImage. Compruebe rápidamente si una forma contiene bytes de imagen o enlaces, optimizando su flujo de trabajo de diseño sin esfuerzo.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Devuelve`verdadero` si la forma tiene bytes de imagen o vincula una imagen.

```csharp
public bool HasImage { get; }
```

## Ejemplos

Muestra cómo guardar todas las imágenes de un documento en el sistema de archivos.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Las formas con el indicador "HasImage" establecido almacenan y muestran todas las imágenes del documento.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

//Recorre cada forma y guarda su imagen.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
