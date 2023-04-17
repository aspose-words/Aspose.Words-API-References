---
title: Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings method
linktitle: get_UseBookFoldPrintingSettings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings method. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via MultiplePages in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words.saving/pdfsaveoptions/get_usebookfoldprintingsettings/
---
## PdfSaveOptions::get_UseBookFoldPrintingSettings method


Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Remarks


If this option is specified, [PageSet](../../fixedpagesaveoptions/get_pageset/) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

## Examples



Shows how to save a document to the PDF format in the form of a book fold. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output PDF in a way that helps us use it to make a booklet.
// Set the "UseBookFoldPrintingSettings" property to "false" to render the PDF normally.
options->set_UseBookFoldPrintingSettings(renderTextAsBookfold);

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
{
    for (const auto& s : System::IterateOver<Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(MultiplePagesType::BookFoldPrinting);
    }
}

// Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
// and the contents will line up in a way that creates a booklet.
doc->Save(ArtifactsDir + u"PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

## See Also

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
