---
title: SaveFormat
second_title: Aspose.Words for .NET API Reference
description: PsSaveOptions property. Specifies the format in which the document will be saved if this save options object is used. Can only be Ps in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Specifies the format in which the document will be saved if this save options object is used. Can only be Ps.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* namespace [Aspose.Words.Saving](../../pssaveoptions/)
* assembly [Aspose.Words](../../../)
