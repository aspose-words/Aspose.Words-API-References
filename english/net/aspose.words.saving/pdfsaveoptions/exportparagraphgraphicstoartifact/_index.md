---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words for .NET API Reference
description: PdfSaveOptions property. Gets or sets a value determining whether a paragraph graphic should be marked as an artifact in C#.
type: docs
weight: 160
url: /net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Gets or sets a value determining whether a paragraph graphic should be marked as an artifact.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Remarks

Default value is `false` and paragraph graphics (underlines, text emphasis, etc.) will be marked as "Span" in the logical structure of the document.

When the value is `true` the paragraph graphics will be marked as "Artifact".

This value is ignored when [`ExportDocumentStructure`](../exportdocumentstructure/) is `false`.

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pdfsaveoptions/)
* assembly [Aspose.Words](../../../)
