---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words para .NET
description: Aprovecha el poder del método ToImage en ImageData para recuperar fácilmente imágenes almacenadas en formas como objetos Image. ¡Mejora tus proyectos sin esfuerzo!
type: docs
weight: 230
url: /es/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Obtiene la imagen almacenada en la forma como unaImage objeto.

```csharp
public Image ToImage()
```

## Observaciones

Un nuevoImage El objeto se crea cada vez que se llama a este método.

Es responsabilidad del llamante disponer del objeto de imagen.

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
