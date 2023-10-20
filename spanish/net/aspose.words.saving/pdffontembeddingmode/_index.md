---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.PdfFontEmbeddingMode enumeración. Especifica cómo Aspose.Words debe incrustar fuentes en C#.
type: docs
weight: 5470
url: /es/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Especifica cómo Aspose.Words debe incrustar fuentes.

```csharp
public enum PdfFontEmbeddingMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words incorpora todas las fuentes. |
| EmbedNonstandard | `1` | Aspose.Words incorpora todas las fuentes excepto las fuentes estándar de Windows Arial y Times New Roman. Sólo las fuentes Arial y Times New Roman se ven afectadas en este modo porque MS Word no incorpora solo estas fuentes al guardar el documento en PDF. |
| EmbedNone | `2` | Aspose.Words no incorpora ninguna fuente. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
