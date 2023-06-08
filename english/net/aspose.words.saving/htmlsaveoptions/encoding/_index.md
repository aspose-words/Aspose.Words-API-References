---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: HtmlSaveOptions Encoding property. Specifies the encoding to use when exporting to HTML MHTML or EPUB. Default value is new UTF8Encodingfalse UTF8 without BOM in C#.
type: docs
weight: 100
url: /net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is `new UTF8Encoding(false)` (UTF-8 without BOM).

```csharp
public Encoding Encoding { get; set; }
```

## Examples

Shows how to use a specific encoding when saving a document to .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specify that we want to export document properties.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
