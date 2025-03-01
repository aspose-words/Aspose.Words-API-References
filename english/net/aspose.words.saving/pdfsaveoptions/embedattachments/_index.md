---
title: PdfSaveOptions.EmbedAttachments
linktitle: EmbedAttachments
articleTitle: EmbedAttachments
second_title: Aspose.Words for .NET
description: Discover PdfSaveOptions' EmbedAttachments property to easily control PDF attachment embedding, enhancing document versatility and user experience.
type: docs
weight: 110
url: /net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

Gets or sets a value determining whether or not to embed attachments to the PDF document.

```csharp
public bool EmbedAttachments { get; set; }
```

## Remarks

Default value is `false` and attachments are not embedded.

When the value is `true` attachments are embedded to the PDF document.

Embedding attachments is not supported when saving to PDF/A and PDF/UA compliance. `false` value will be used automatically.

Embedding attachments is not supported when encryption is enabled. `false` value will be used automatically.

## Examples

Shows how to add embed attachments to the PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
