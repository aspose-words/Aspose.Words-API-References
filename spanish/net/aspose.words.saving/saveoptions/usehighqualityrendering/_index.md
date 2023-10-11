---
title: SaveOptions.UseHighQualityRendering
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOptions propiedad. Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad es decir lentos.
type: docs
weight: 200
url: /es/net/aspose.words.saving/saveoptions/usehighqualityrendering/
---
## SaveOptions.UseHighQualityRendering property

Obtiene o establece un valor que determina si se utilizan o no algoritmos de renderizado de alta calidad (es decir, lentos).

```csharp
public bool UseHighQualityRendering { get; set; }
```

### Observaciones

El valor predeterminado es`FALSO` .

Esta propiedad se utiliza cuando el documento se exporta a formatos de imagen: Tiff ,Png ,Bmp , Jpeg ,Emf.

### Ejemplos

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
* espacio de nombres [Aspose.Words.Saving](../../saveoptions/)
* asamblea [Aspose.Words](../../../)


