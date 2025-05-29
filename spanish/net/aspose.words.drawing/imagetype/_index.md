---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.ImageType para gestionar fácilmente los formatos de imagen en documentos de Microsoft Word. ¡Mejore el atractivo visual de su documento!
type: docs
weight: 1410
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
| Pict | `4` | PICT de Macintosh. Una imagen existente se conservará en un documento, pero no se permite insertar nuevas imágenes PICT en un documento. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Gráficos de red portátiles. |
| Bmp | `7` | Mapa de bits de Windows. |
| Eps | `8` | PostScript encapsulado. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## Ejemplos

Muestra cómo leer imágenes WebP.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Muestra cómo agregar una imagen a una forma y verificar su tipo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Ver también

* property [ImageType](../imagedata/imagetype/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
