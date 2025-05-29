---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.PdfTextCompression para una compresión eficiente de contenido PDF, mejorando el tamaño y el rendimiento del archivo y preservando la calidad.
type: docs
weight: 6330
url: /es/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Especifica un tipo de compresión que se aplica a todo el contenido del archivo PDF, excepto las imágenes.

```csharp
public enum PdfTextCompression
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Sin compresión. |
| Flate | `1` | Compresión plana (ZIP). |

## Ejemplos

Muestra cómo aplicar compresión de texto al guardar un documento en PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Establezca la propiedad "TextCompression" en "PdfTextCompression.None" para no aplicar ninguna
//compresión a texto cuando guardamos el documento en PDF.
// Establezca la propiedad "TextCompression" en "PdfTextCompression.Flate" para aplicar la compresión ZIP
// al texto al guardar el documento en PDF. Cuanto más grande sea el documento, mayor será el impacto.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
