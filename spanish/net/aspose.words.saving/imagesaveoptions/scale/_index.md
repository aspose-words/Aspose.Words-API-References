---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words para .NET
description: Descubra la propiedad Escala de ImageSaveOptions para ajustar sin esfuerzo el factor de zoom de sus imágenes, mejorando la calidad y la personalización.
type: docs
weight: 150
url: /es/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Obtiene o establece el factor de zoom para las imágenes generadas.

```csharp
public float Scale { get; set; }
```

## Observaciones

El valor predeterminado es 1.0. El valor debe ser mayor que 0.

## Ejemplos

Muestra cómo representar un objeto de Office Math en un archivo de imagen en el sistema de archivos local.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Cree un objeto "ImageSaveOptions" para pasar al método "Guardar" del renderizador de nodos para modificar
// cómo convierte el nodo OfficeMath en una imagen.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Establezca la propiedad "Escala" en 5 para representar el objeto a cinco veces su tamaño original.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

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

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
