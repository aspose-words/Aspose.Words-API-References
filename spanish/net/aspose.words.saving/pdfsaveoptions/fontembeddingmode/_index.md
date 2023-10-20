---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words para .NET
description: PdfSaveOptions FontEmbeddingMode propiedad. Especifica el modo de incrustación de fuente en C#.
type: docs
weight: 170
url: /es/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Especifica el modo de incrustación de fuente.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Observaciones

El valor predeterminado esEmbedAll.

Esta configuración solo funciona para el texto en codificación ANSI (Windows-1252). Si el documento contiene texto que no es ANSI, se incrustarán las fuentes correspondientes independientemente de esta configuración.

La compatibilidad con PDF/A y PDF/UA requiere que todas las fuentes estén incrustadas. EmbedAll El valor se utilizará automáticamente al guardar en PDF/A y PDF/UA.

## Ejemplos

Muestra cómo configurar Aspose.Words para omitir la incorporación de fuentes Arial y Times New Roman en un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" es una fuente estándar y "Courier New" es una fuente no estándar.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "EmbedFullFonts" en "true" para incrustar cada glifo de cada fuente incrustada en el PDF de salida.
options.EmbedFullFonts = true;

// Establece la propiedad "FontEmbeddingMode" en "EmbedAll" para incrustar todas las fuentes en el PDF de salida.
// Establezca la propiedad "FontEmbeddingMode" en "EmbedNonstandard" para permitir solo la incrustación de fuentes no estándar en el PDF de salida.
// Establece la propiedad "FontEmbeddingMode" en "EmbedNone" para no incrustar ninguna fuente en el PDF de salida.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
    case PdfFontEmbeddingMode.EmbedAll:
        Assert.That(1000000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNonstandard:
        Assert.That(480000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNone:
        Assert.That(4255, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Ver también

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
