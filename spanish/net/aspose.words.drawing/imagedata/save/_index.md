---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words para .NET
description: Guarda imágenes fácilmente con el método ImageData Save. Optimiza tu flujo de trabajo almacenando imágenes directamente en la secuencia que elijas fácilmente.
type: docs
weight: 200
url: /es/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Guarda la imagen en la secuencia especificada.

```csharp
public void Save(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia donde guardar la imagen. |

## Observaciones

¿Es responsabilidad del llamador disponer del objeto de flujo?

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

---

## Save(*string*) {#save_1}

Guarda la imagen en un archivo.

```csharp
public void Save(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre del archivo donde guardar la imagen. |

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

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
