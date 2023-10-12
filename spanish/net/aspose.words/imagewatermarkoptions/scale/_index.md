---
title: ImageWatermarkOptions.Scale
second_title: Referencia de API de Aspose.Words para .NET
description: ImageWatermarkOptions propiedad. Obtiene o establece el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0  auto.
type: docs
weight: 30
url: /es/net/aspose.words/imagewatermarkoptions/scale/
---
## ImageWatermarkOptions.Scale property

Obtiene o establece el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0 - auto.

```csharp
public double Scale { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando el argumento estaba fuera del rango de valores válidos. |

### Observaciones

Los valores válidos oscilan entre 0 y 65,5 inclusive.

Escala automática significa que la marca de agua se escalará a su ancho máximo y alto máximo en relación con los márgenes de la página.

### Ejemplos

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

```csharp
Document doc = new Document();

            // Modifica la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
            // luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ver también

* class [ImageWatermarkOptions](../)
* espacio de nombres [Aspose.Words](../../imagewatermarkoptions/)
* asamblea [Aspose.Words](../../../)


