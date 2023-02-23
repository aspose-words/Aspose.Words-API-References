---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET API Reference
description: PsSaveOptions property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout if it is specified via MultiplePages in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/).

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Remarks

If this option is specified, [`PageSet`](../../fixedpagesaveoptions/pageset/) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

## Examples

Shows how to save a document to the Postscript format in the form of a book fold.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Create a "PsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to PostScript.
// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output Postscript document in a way that helps us make a booklet out of it.
// Set the "UseBookFoldPrintingSettings" property to "false" to save the document normally.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
// and the contents will line up in a way that creates a booklet.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### See Also

* class [PsSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pssaveoptions/)
* assembly [Aspose.Words](../../../)
