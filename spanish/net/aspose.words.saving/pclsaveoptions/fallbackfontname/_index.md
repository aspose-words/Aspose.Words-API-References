---
title: PclSaveOptions.FallbackFontName
linktitle: FallbackFontName
articleTitle: FallbackFontName
second_title: Aspose.Words para .NET
description: Descubra la propiedad PclSaveOptions FallbackFontName, que garantiza una impresión perfecta con una fuente predeterminada cuando la fuente deseada no está disponible.
type: docs
weight: 20
url: /es/net/aspose.words.saving/pclsaveoptions/fallbackfontname/
---
## PclSaveOptions.FallbackFontName property

Nombre de la fuente que se utilizará si no se encuentra la fuente esperada en la impresora y en las colecciones de fuentes integradas.

```csharp
public string FallbackFontName { get; set; }
```

## Observaciones

Si no se encuentra ninguna alternativa, se genera una advertencia y se utiliza la fuente "Arial".

## Ejemplos

Muestra cómo declarar una fuente que una impresora aplicará al texto impreso como sustituto si su fuente original no está disponible.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.FallbackFontName = "Times New Roman";

// Este documento le indicará a la impresora que aplique "Times New Roman" al texto con la fuente faltante.
// Si "Times New Roman" tampoco está disponible, la impresora utilizará de forma predeterminada la fuente "Arial".
doc.Save(ArtifactsDir + "PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

### Ver también

* class [PclSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
