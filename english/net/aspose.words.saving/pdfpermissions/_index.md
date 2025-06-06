---
title: PdfPermissions Enum
linktitle: PdfPermissions
articleTitle: PdfPermissions
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.PdfPermissions enum for controlling user access on encrypted PDFs. Enhance security and manage document operations effectively.
type: docs
weight: 6320
url: /net/aspose.words.saving/pdfpermissions/
---
## PdfPermissions enumeration

Specifies the operations that are allowed to a user on an encrypted PDF document.

```csharp
[Flags]
public enum PdfPermissions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DisallowAll | `0` | Disallows all operations on the PDF document. This is the default value. |
| AllowAll | `FFFF` | Allows all operations on the PDF document. |
| ContentCopy | `10` | Copy or otherwise extract text and graphics from the document by operations other than that controlled by ContentCopyForAccessibility. |
| ContentCopyForAccessibility | `200` | Extract text and graphics (in support of accessibility to users with disabilities or for other purposes). |
| ModifyContents | `8` | Modify the contents of the document by operations other than those controlled by ModifyAnnotations, FillIn, and DocumentAssembly. |
| ModifyAnnotations | `20` | Add or modify text annotations, fill in interactive form fields, and, if ModifyContents is also set, create or modify interactive form fields (including signature fields). |
| FillIn | `100` | Fill in existing interactive form fields (including signature fields), even if ModifyContents is clear. |
| DocumentAssembly | `400` | Assemble the document (insert, rotate, or delete pages and create document outline items or thumbnail images), even if ModifyContents is clear. |
| Printing | `4` | Print the document (possibly not at the highest quality level, depending on whether HighResolutionPrinting is also set). |
| HighResolutionPrinting | `804` | Print the document to a representation from which a faithful digital copy of the PDF content could be generated, based on an implementation-dependent algorithm. When this flag is clear (and Printing is set), printing shall be limited to a low-level representation of the appearance, possibly of degraded quality. |

## Examples

Shows how to set permissions on a saved PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Extend permissions to allow the editing of annotations.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Enable encryption via the "EncryptionDetails" property.
saveOptions.EncryptionDetails = encryptionDetails;

// When we open this document, we will need to provide the password before accessing its contents.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
