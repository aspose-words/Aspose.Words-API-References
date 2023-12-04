---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET
description: PdfSaveOptions UseBookFoldPrintingSettings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout if it is specified via MultiplePages in C#.
type: docs
weight: 310
url: /net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/).

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Remarks

If this option is specified, [`PageSet`](../../fixedpagesaveoptions/pageset/) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

## Examples

Shows how to save a document to the PDF format in the form of a book fold.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output PDF in a way that helps us use it to make a booklet.
// Set the "UseBookFoldPrintingSettings" property to "false" to render the PDF normally.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
// and the contents will line up in a way that creates a booklet.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
