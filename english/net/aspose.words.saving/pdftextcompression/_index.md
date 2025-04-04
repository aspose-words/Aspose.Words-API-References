---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.PdfTextCompression enum for efficient PDF content compression, enhancing file size and performance while preserving quality.
type: docs
weight: 6310
url: /net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Specifies a type of compression applied to all content in the PDF file except images.

```csharp
public enum PdfTextCompression
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No compression. |
| Flate | `1` | Flate (ZIP) compression. |

## Examples

Shows how to apply text compression when saving a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
// compression to text when we save the document to PDF.
// Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
// to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
