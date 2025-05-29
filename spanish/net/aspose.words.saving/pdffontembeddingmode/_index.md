---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.PdfFontEmbeddingMode para una incrustación óptima de fuentes en archivos PDF. Mejore la calidad del documento y garantice una visualización uniforme del texto.
type: docs
weight: 6260
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
| EmbedAll | `0` | Aspose.Words integra todas las fuentes. |
| EmbedNonstandard | `1` | Aspose.Words incorpora todas las fuentes excepto las fuentes estándar de Windows Arial y Times New Roman. Solo las fuentes Arial y Times New Roman se ven afectadas en este modo porque MS Word no incorpora solo estas fuentes al guardar el documento en PDF. |
| EmbedNone | `2` | Aspose.Words no incorpora ninguna fuente. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
