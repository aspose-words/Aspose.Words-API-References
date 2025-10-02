---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: Aspose.Words for .NET
description: Discover the PdfSaveOptions ExportParagraphGraphicsToArtifact property to control paragraph graphics as artifacts, enhancing your document's visual clarity.
type: docs
weight: 170
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

## Examples

Shows how to export paragraph graphics as artifact (underlines, text emphasis, etc.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
