---
title: ImageSaveOptions.ImageColorMode
second_title: Referencia de API de Aspose.Words para .NET
description: ImageSaveOptions propiedad. Obtiene o establece el modo de color para las imágenes generadas.
type: docs
weight: 50
url: /es/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Obtiene o establece el modo de color para las imágenes generadas.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

### Observaciones

Esta propiedad tiene efecto sólo al guardar en formatos de imagen rasterizada.

El valor predeterminado esNone.

### Ejemplos

Muestra cómo configurar un modo de color al renderizar documentos.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
            builder.Writeln("Hello world!");
            builder.InsertImage(ImageDir + "Logo.jpg");

            Assert.That(20000, Is.LessThan(new FileInfo(ImageDir + "Logo.jpg").Length));

            // Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
            // selecciona un modo de color para la imagen que generará la operación de guardado.
            // Si configuramos la propiedad "ImageColorMode" en "ImageColorMode.BlackAndWhite",
            // la operación de guardar aplicará reducción de color en escala de grises mientras renderiza el documento.
            // Si configuramos la propiedad "ImageColorMode" en "ImageColorMode.Grayscale",
            // la operación de guardar convertirá el documento en una imagen monocromática.
            // Si configuramos la propiedad "ImageColorMode" en "Ninguno", la operación de guardado aplicará el método predeterminado
            // y conservar todos los colores del documento en la imagen de salida.
            ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
            imageSaveOptions.ImageColorMode = imageColorMode;

            doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);

#if NET48 || JAVA
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(150000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#elif NET5_0_OR_GREATER
            switch (imageColorMode)
            {
                case ImageColorMode.None:
                    Assert.That(120000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.Grayscale:
                    Assert.That(80000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
                case ImageColorMode.BlackAndWhite:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.ColorMode.png").Length));
                    break;
            }
#endif
```

### Ver también

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../imagesaveoptions/)
* asamblea [Aspose.Words](../../../)


