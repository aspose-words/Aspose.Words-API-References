---
title: ImageWatermarkOptions.IsWashout
second_title: Referencia de API de Aspose.Words para .NET
description: ImageWatermarkOptions propiedad. Obtiene o establece un valor booleano que es responsable del efecto de eliminación de la marca de agua. El valor predeterminado esverdadero .
type: docs
weight: 20
url: /es/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Obtiene o establece un valor booleano que es responsable del efecto de eliminación de la marca de agua. El valor predeterminado es`verdadero` .

```csharp
public bool IsWashout { get; set; }
```

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


