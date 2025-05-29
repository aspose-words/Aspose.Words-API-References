---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words para .NET
description: Descubra el método ImageSaveOptions Clone para crear sin esfuerzo un clon profundo de sus objetos, mejorando su eficiencia y flexibilidad de codificación.
type: docs
weight: 210
url: /es/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Crea un clon profundo de este objeto.

```csharp
public ImageSaveOptions Clone()
```

## Ejemplos

Muestra cómo seleccionar una velocidad de bits por píxel con la que convertir un documento en una imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// seleccione un formato de píxel para la imagen que generará la operación de guardado.
//Varias tasas de bits por píxel afectarán la calidad y el tamaño del archivo de la imagen generada.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

//Podemos clonar instancias de ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
