---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words para .NET
description: Descubre la propiedad FontEmbeddingMode de PdfSaveOptions para optimizar la incrustación de fuentes en tus PDF. ¡Mejora la calidad y la compatibilidad de tus documentos sin esfuerzo!
type: docs
weight: 170
url: /es/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Especifica el modo de incrustación de fuentes.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Observaciones

El valor predeterminado esEmbedAll.

Esta configuración solo funciona con texto codificado ANSI (Windows-1252). Si el documento contiene texto no ANSI, se incrustarán las fuentes correspondientes independientemente de esta configuración.

La compatibilidad con PDF/A y PDF/UA requiere que todas las fuentes estén incorporadas. EmbedAll El valor se utilizará automáticamente al guardar en PDF/A y PDF/UA.

## Ejemplos

Muestra cómo configurar Aspose.Words para omitir la incrustación de fuentes Arial y Times New Roman en un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" es una fuente estándar y "Courier New" es una fuente no estándar.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Establezca la propiedad "EmbedFullFonts" en "true" para incrustar cada glifo de cada fuente incrustada en el PDF de salida.
options.EmbedFullFonts = true;
// Establezca la propiedad "FontEmbeddingMode" en "EmbedAll" para incrustar todas las fuentes en el PDF de salida.
// Establezca la propiedad "FontEmbeddingMode" en "EmbedNonstandard" para permitir únicamente la incrustación de fuentes no estándar en el PDF de salida.
// Establezca la propiedad "FontEmbeddingMode" en "EmbedNone" para no incrustar ninguna fuente en el PDF de salida.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Ver también

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
