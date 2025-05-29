---
title: ImageWatermarkOptions.IsWashout
linktitle: IsWashout
articleTitle: IsWashout
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsWashout de ImageWatermarkOptions. Controle fácilmente el efecto de lavado de su marca de agua con esta sencilla configuración booleana.
type: docs
weight: 20
url: /es/net/aspose.words/imagewatermarkoptions/iswashout/
---
## ImageWatermarkOptions.IsWashout property

Obtiene o establece un valor booleano que es responsable del efecto de lavado de la marca de agua. El valor predeterminado es`verdadero` .

```csharp
public bool IsWashout { get; set; }
```

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
