---
title: Enum ImageType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.ImageType enumeración. Especifica el tipo formato de una imagen en un documento de Microsoft Word.
type: docs
weight: 950
url: /es/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Especifica el tipo (formato) de una imagen en un documento de Microsoft Word.

```csharp
public enum ImageType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| NoImage | `0` | No hay datos de imagen. |
| Unknown | `1` | Un tipo de imagen desconocido o un tipo de imagen que no se puede almacenar directamente dentro de un documento de Microsoft Word. |
| Emf | `2` | Metarchivo mejorado de Windows. |
| Wmf | `3` | Metarchivo de Windows. |
| Pict | `4` | Macintosh IMAGEN. Una imagen existente se conservará en un documento, pero no se admite la inserción de nuevas imágenes PICT en un documento. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Gráficos de red portátiles. |
| Bmp | `7` | Mapa de bits de Windows. |

### Ejemplos

Muestra cómo agregar una imagen a una forma y comprobar su tipo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // La imagen en la URL es un .gif. Insertarlo en un documento lo convierte en un .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Ver también

* property [ImageType](../imagedata/imagetype/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


