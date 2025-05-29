---
title: ImageSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveFormat de ImageSaveOptions para guardar documentos fácilmente en formatos como TIFF, PNG, JPEG y más. ¡Mejore su flujo de trabajo hoy mismo!
type: docs
weight: 140
url: /es/net/aspose.words.saving/imagesaveoptions/saveformat/
---
## ImageSaveOptions.SaveFormat property

Especifica el formato en el que se guardarán las páginas o formas del documento renderizado si se utiliza este objeto de opciones de guardado. Puede ser un ráster Tiff ,Png ,Bmp , Jpeg o vectorEmf ,Eps , WebP ,Svg .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Observaciones

El número de otras opciones depende del formato seleccionado.

También es posible guardar en SVG tanto mediante[`ImageSaveOptions`](../) y vía[`SvgSaveOptions`](../../svgsaveoptions/).

## Ejemplos

Muestra cómo editar la imagen mientras Aspose.Words convierte un documento en uno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// edita la imagen mientras se procesa la operación de guardado.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    //Podemos ajustar estas propiedades para cambiar el brillo y el contraste de la imagen.
    //Ambos están en una escala de 0 a 1 y están en 0,5 por defecto.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    //Podemos ajustar la resolución horizontal y vertical con estas propiedades.
    // Esto afectará las dimensiones de la imagen.
    //El valor predeterminado para estas propiedades es 96.0, para una resolución de 96 ppp.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    Podemos escalar la imagen usando esta propiedad. El valor predeterminado es 1.0, para un escalado del 100%.
    //Podemos usar esta propiedad para negar cualquier cambio en las dimensiones de la imagen que pudiera causar el cambio de la resolución.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
