---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words para .NET
description: PdfSaveOptions TextCompression propiedad. Especifica el tipo de compresión que se utilizará para todo el contenido textual del documento en C#.
type: docs
weight: 290
url: /es/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Especifica el tipo de compresión que se utilizará para todo el contenido textual del documento.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Observaciones

El valor predeterminado esFlate.

Aumenta significativamente el tamaño de salida al guardar un documento sin compresión.

## Ejemplos

Muestra cómo aplicar compresión de texto al guardar un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establece la propiedad "TextCompression" en "PdfTextCompression.None" para no aplicar ninguna
// compresión a texto cuando guardamos el documento en PDF.
// Establece la propiedad "TextCompression" en "PdfTextCompression.Flate" para aplicar compresión ZIP
// al texto cuando guardamos el documento en PDF. Cuanto más grande sea el documento, mayor será el impacto que esto tendrá.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Ver también

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
