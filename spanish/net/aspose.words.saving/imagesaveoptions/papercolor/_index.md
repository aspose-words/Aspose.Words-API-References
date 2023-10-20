---
title: ImageSaveOptions.PaperColor
linktitle: PaperColor
articleTitle: PaperColor
second_title: Aspose.Words para .NET
description: ImageSaveOptions PaperColor propiedad. Obtiene o establece el color de fondo papel para las imágenes generadas en C#.
type: docs
weight: 110
url: /es/net/aspose.words.saving/imagesaveoptions/papercolor/
---
## ImageSaveOptions.PaperColor property

Obtiene o establece el color de fondo (papel) para las imágenes generadas.

El valor predeterminado esWhite.

```csharp
public Color PaperColor { get; set; }
```

## Observaciones

Al representar páginas de un documento que especifica su propio color de fondo, , el color de fondo del documento anulará el color especificado por esta propiedad.

## Ejemplos

Representa una página de un documento de Word en una imagen con fondo transparente o coloreado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);

// Establece la propiedad "PaperColor" en un color transparente para aplicar un color transparente
// fondo del documento mientras lo representa en una imagen.
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Establece la propiedad "PaperColor" en un color opaco para aplicar ese color
// como fondo del documento cuando lo representamos en una imagen.
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### Ver también

* class [ImageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
