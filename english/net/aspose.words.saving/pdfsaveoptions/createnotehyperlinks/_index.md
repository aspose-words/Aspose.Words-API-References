---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words for .NET
description: Enhance your PDFs with PdfSaveOptions' CreateNoteHyperlinks. Convert footnotes and endnotes into clickable links for easy navigation. Default: false.
type: docs
weight: 50
url: /net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is `false`.

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Examples

Shows how to make footnotes and endnotes function as hyperlinks.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "CreateNoteHyperlinks" property to "true" to turn all footnote/endnote symbols
// in the text act as links that, upon clicking, take us to their respective footnotes/endnotes.
// Set the "CreateNoteHyperlinks" property to "false" not to have footnote/endnote symbols link to anything.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
