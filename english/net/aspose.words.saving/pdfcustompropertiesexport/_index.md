---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words for .NET
description: Discover how the Aspose.Words.PdfCustomPropertiesExport enum enhances PDF exports by customizing document properties for optimal results.
type: docs
weight: 6220
url: /net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

Specifies the way [`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) are exported to PDF file.

```csharp
public enum PdfCustomPropertiesExport
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No custom properties are exported. |
| Standard | `1` | Custom properties are exported as entries in /Info dictionary. |
| Metadata | `2` | Custom properties are Metadata. |

## Examples

Shows how to export custom properties while converting a document to PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.None" to discard
// custom document properties as we save the document to .PDF.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Standard"
// to preserve custom properties within the output PDF document.
// Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
// to preserve custom properties in an XMP packet.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
