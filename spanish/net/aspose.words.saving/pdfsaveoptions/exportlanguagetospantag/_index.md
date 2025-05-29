---
title: PdfSaveOptions.ExportLanguageToSpanTag
linktitle: ExportLanguageToSpanTag
articleTitle: ExportLanguageToSpanTag
second_title: Aspose.Words para .NET
description: Descubra la propiedad ExportLanguageToSpanTag de PdfSaveOptions. Controle la exportación del idioma del texto con etiquetas Span para mejorar la estructura y la accesibilidad del documento.
type: docs
weight: 150
url: /es/net/aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/
---
## PdfSaveOptions.ExportLanguageToSpanTag property

Obtiene o establece un valor que determina si se debe crear o no una etiqueta "Span" en la estructura del documento para exportar el idioma del texto.

```csharp
public bool ExportLanguageToSpanTag { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` el atributo "Lang" se adjunta a una secuencia de contenido marcado en un flujo de contenido de página.

Cuando el valor es`verdadero` La etiqueta "Span" se crea para el texto con un idioma no predeterminado y el atributo "Lang" se adjunta a esta etiqueta.

Este valor se ignora cuando[`ExportDocumentStructure`](../exportdocumentstructure/) es`FALSO` .

## Ejemplos

Muestra cómo crear una etiqueta "Span" en la estructura del documento para exportar el idioma del texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hola mundo!");

PdfSaveOptions saveOptions = new PdfSaveOptions
{
    // Tenga en cuenta que, cuando "ExportDocumentStructure" es falso, se ignora "ExportLanguageToSpanTag".
    ExportDocumentStructure = true, ExportLanguageToSpanTag = true
};

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportLanguageToSpanTag.pdf", saveOptions);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
