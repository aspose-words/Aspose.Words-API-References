---
title: ImageWatermarkOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words para .NET
description: Descubra la propiedad Escala de ImageWatermarkOptions para ajustar fácilmente la escala de la imagen y optimizar la marca de agua. El valor predeterminado es 0 (automático) para una integración perfecta.
type: docs
weight: 30
url: /es/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Obtiene o establece el factor de escala expresado como fracción de la imagen. El valor predeterminado es 0 - auto.

```csharp
public double Scale { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando el argumento está fuera del rango de valores válidos. |

## Observaciones

Los valores válidos oscilan entre 0 y 65,5 inclusive.

Escala automática significa que la marca de agua se escalará a su ancho máximo y altura máxima en relación con los márgenes de la página.

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

* class [ImageWatermarkOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
