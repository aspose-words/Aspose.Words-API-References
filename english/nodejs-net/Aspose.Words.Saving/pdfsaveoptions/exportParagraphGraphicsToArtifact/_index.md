---
title: PdfSaveOptions.exportParagraphGraphicsToArtifact property
linktitle: exportParagraphGraphicsToArtifact property
articleTitle: exportParagraphGraphicsToArtifact property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.exportParagraphGraphicsToArtifact property. Gets or sets a value determining whether a paragraph graphic should be marked as an artifact."
type: docs
weight: 160
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/exportParagraphGraphicsToArtifact/
---

## PdfSaveOptions.exportParagraphGraphicsToArtifact property

Gets or sets a value determining whether a paragraph graphic should be marked as an artifact.


```js
get exportParagraphGraphicsToArtifact(): boolean
```

### Remarks

Default value is ``False`` and paragraph graphics (underlines, text emphasis, etc.)
will be marked as "Span" in the logical structure of the document.

When the value is ``True`` the paragraph graphics will be marked as "Artifact".

This value is ignored when [PdfSaveOptions.exportDocumentStructure](../exportDocumentStructure/) is ``False``. 




### Examples

Shows how to export paragraph graphics as artifact (underlines, text emphasis, etc.).

```js
let doc = new aw.Document(base.myDir + "PDF artifacts.docx");

let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.exportDocumentStructure = true;
saveOptions.exportParagraphGraphicsToArtifact = true;
saveOptions.textCompression = aw.Saving.PdfTextCompression.None;

doc.save(base.artifactsDir + "PdfSaveOptions.exportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

