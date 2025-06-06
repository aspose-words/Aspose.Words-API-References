---
title: SaveOptions.UseAntiAliasing
linktitle: UseAntiAliasing
articleTitle: UseAntiAliasing
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveOptions UseAntiAliasing para mejorar la calidad de renderizado. Controle el suavizado para obtener imágenes más fluidas y un mejor rendimiento.
type: docs
weight: 200
url: /es/net/aspose.words.saving/saveoptions/useantialiasing/
---
## SaveOptions.UseAntiAliasing property

Obtiene o establece un valor que determina si se debe utilizar o no suavizado para la representación.

```csharp
public bool UseAntiAliasing { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` . Cuando este valor se establece en`verdadero` El suavizado se utiliza para la representación.

Esta propiedad se utiliza cuando el documento se exporta a los siguientes formatos: Tiff ,Png ,Bmp , Jpeg ,Emf . Cuando el documento se exporta a Html ,Mhtml , Epub ,Azw3 oMobiFormatos: esta opción se utiliza para imágenes rasterizadas.

## Ejemplos

Muestra cómo mejorar la calidad de un documento renderizado con SaveOptions.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 60;
builder.Writeln("Some text.");

SaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
doc.Save(ArtifactsDir + "Document.ImageSaveOptions.Default.jpg", options);

options.UseAntiAliasing = true;
options.UseHighQualityRendering = true;

doc.Save(ArtifactsDir + "Document.ImageSaveOptions.HighQuality.jpg", options);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
