---
title: ImageWatermarkOptions Class
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.ImageWatermarkOptions. Personalice sus marcas de agua de imagen fácilmente con opciones versátiles para una mejor presentación de documentos.
type: docs
weight: 3670
url: /es/net/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class

Contiene opciones que se pueden especificar al agregar una marca de agua con imagen.

Para obtener más información, visite el[Trabajar con marca de agua](https://docs.aspose.com/words/net/working-with-watermark/) Artículo de documentación.

```csharp
public class ImageWatermarkOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ImageWatermarkOptions](imagewatermarkoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [IsWashout](../../aspose.words/imagewatermarkoptions/iswashout/) { get; set; } | Obtiene o establece un valor booleano que es responsable del efecto de lavado de la marca de agua. El valor predeterminado es`verdadero` . |
| [Scale](../../aspose.words/imagewatermarkoptions/scale/) { get; set; } | Obtiene o establece el factor de escala expresado como fracción de la imagen. El valor predeterminado es 0 - auto. |

## Ejemplos

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

```csharp
Document doc = new Document();

            // Modifique la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
            // luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            //Tenemos diferentes opciones para insertar imágenes:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
