---
title: SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: Discover how to use the SaveOptions SaveFormat property to effortlessly choose your document's save format for optimal flexibility and control.
type: docs
weight: 130
url: /net/aspose.words.saving/saveoptions/saveformat/
---
## SaveOptions.SaveFormat property

Specifies the format in which the document will be saved if this save options object is used.

```csharp
public abstract SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
