---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica si Aspose.Words escala las imágenes al tamaño de la forma límite cuando se exportan a HTML MHTML o EPUB. El valor predeterminado esverdadero .
type: docs
weight: 450
url: /es/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Especifica si Aspose.Words escala las imágenes al tamaño de la forma límite cuando se exportan a HTML, MHTML o EPUB. El valor predeterminado es`verdadero` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### Observaciones

Una imagen en un documento de Microsoft Word es una forma. La forma tiene un tamaño y la imagen tiene su propio tamaño. Los tamaños no están directamente relacionados. Por ejemplo, la imagen puede tener 1024x786 píxeles, pero la forma que muestra esta imagen puede tener 400x300 puntos.

Para mostrar una imagen en el navegador, debe escalarse al tamaño de la forma. El`ScaleImageToShapeSize` Controles de propiedad donde tiene lugar el escalado de la imagen : en Aspose.Words durante la exportación a HTML o en el navegador al mostrar el documento.

Cuando`ScaleImageToShapeSize` es`verdadero` , Aspose.Words escala la imagen mediante un escalado de alta calidad durante la exportación a HTML. Cuando`ScaleImageToShapeSize` es`falso`la imagen sale con su tamaño original y el navegador tiene que escalarla.

En general, los navegadores realizan un escalado rápido y de mala calidad. Como resultado, normalmente obtendrá una mejor calidad de visualización en el navegador y un tamaño de archivo más pequeño cuando`ScaleImageToShapeSize` es`verdadero` , pero mejor calidad de impresión y conversión más rápida cuando`ScaleImageToShapeSize` es`falso`.

### Ejemplos

Muestra cómo deshabilitar la escala de imágenes a sus dimensiones de forma principal al guardar en .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Inserte una forma que contenga una imagen y luego haga esa forma considerablemente más pequeña que la imagen.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // Guardar un documento que contiene formas con imágenes en HTML creará un archivo de imagen en el sistema de archivos local
            // para cada una de esas formas. El documento HTML de salida utilizará <image> etiquetas para vincular y mostrar estas imágenes.
            // Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para determinar
            // si escalar todas las imágenes que están dentro de las formas al tamaño de sus formas.
            // Establecer el indicador "ScaleImageToShapeSize" en "true" reducirá todas las imágenes
            // al tamaño de la forma que lo contiene, de modo que ninguna imagen guardada sea más grande de lo que requiere el documento.
            // Establecer el indicador "ScaleImageToShapeSize" en "falso" preservará los tamaños originales de estas imágenes,
            // que ocupará más espacio a cambio de preservar la calidad de la imagen.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Ver también

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


