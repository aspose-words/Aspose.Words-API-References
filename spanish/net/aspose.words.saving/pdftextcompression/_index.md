---
title: Enum PdfTextCompression
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.PdfTextCompression enumeración. Especifica un tipo de compresión aplicada a todo el contenido del archivo PDF excepto las imágenes.
type: docs
weight: 5530
url: /es/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Especifica un tipo de compresión aplicada a todo el contenido del archivo PDF excepto las imágenes.

```csharp
public enum PdfTextCompression
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Sin compresión. |
| Flate | `1` | Compresión plana (ZIP). |

### Ejemplos

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


