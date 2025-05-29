---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ScaleImageToShapeSize de HtmlSaveOptions optimiza el escalado de imágenes en Aspose.Words para exportaciones HTML, MHTML o EPUB. ¡Mejore sus documentos!
type: docs
weight: 470
url: /es/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Especifica si Aspose.Words escala las imágenes al tamaño de la forma delimitadora al exportar a HTML, MHTML o EPUB. El valor predeterminado es`verdadero` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Observaciones

Una imagen en un documento de Microsoft Word es una forma. La forma tiene un tamaño, y la imagen tiene el suyo. Los tamaños no están directamente relacionados. Por ejemplo, la imagen puede tener 1024x786 píxeles, pero la forma que la muestra puede tener 400x300 puntos.

Para poder mostrar una imagen en el navegador, es necesario escalarla al tamaño de la forma. `ScaleImageToShapeSize` La propiedad controla dónde se lleva a cabo el escalado de la imagen : en Aspose.Words durante la exportación a HTML o en el navegador al mostrar el documento.

Cuando`ScaleImageToShapeSize` es`verdadero` La imagen se escala mediante Aspose.Words con escalado de alta calidad durante la exportación a HTML.`ScaleImageToShapeSize` es`FALSO`, la imagen se muestra con su tamaño original y el navegador tiene que escalarla.

En general, los navegadores realizan un escalado rápido y de baja calidad. Como resultado, normalmente obtendrá una mejor calidad de visualización en el navegador y un tamaño de archivo menor.`ScaleImageToShapeSize` es`verdadero` , pero mejor calidad de impresión y conversión más rápida cuando`ScaleImageToShapeSize` es`FALSO`.

Además de las formas que contienen imágenes raster individuales, esta opción también afecta a las formas de grupo que constan de x000d_ imágenes raster. Si`ScaleImageToShapeSize` es`FALSO` y una forma de grupo contiene imágenes rasterizadas cuya resolución intrínseca es mayor que el valor especificado en[`ImageResolution`](../imageresolution/)Aspose.Words aumentará la resolución de renderizado de ese grupo. Esto permite conservar mejor la calidad de las imágenes agrupadas de alta resolución al guardarlas en HTML.

## Ejemplos

Muestra cómo deshabilitar el escalado de imágenes a las dimensiones de su forma principal al guardarlas en .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una forma que contenga una imagen y luego haga que esa forma sea considerablemente más pequeña que la imagen.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// Guardar un documento que contiene formas con imágenes en HTML creará un archivo de imagen en el sistema de archivos local
// para cada forma. El documento HTML de salida usará etiquetas <image> para vincular y mostrar estas imágenes.
// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para determinar
// si escalar todas las imágenes que están dentro de formas a los tamaños de sus formas.
// Establecer el indicador "ScaleImageToShapeSize" en "verdadero" reducirá cada imagen
// al tamaño de la forma que lo contiene, de modo que ninguna imagen guardada será más grande de lo que el documento requiere.
// Establecer el indicador "ScaleImageToShapeSize" en "falso" conservará los tamaños originales de estas imágenes,
// lo que ocupará más espacio a cambio de preservar la calidad de la imagen.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Ver también

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
