---
title: get_UseBookFoldPrintingSettings
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via MultiplePages.
type: docs
weight: 53
url: /cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## Remarks


If this option is specified, [PageSet](../../fixedpagesaveoptions/get_pageset/) is ignored when saving. This behavior matches MS Word. If book fold printing settings are not specified in page setup, this option will have no effect.

## Examples



Shows how to save a document to the XPS format in the form of a book fold. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Paragraphs.docx");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
auto xpsOptions = MakeObject<XpsSaveOptions>(SaveFormat::Xps);

// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output XPS in a way that helps us use it to make a booklet.
// Set the "UseBookFoldPrintingSettings" property to "false" to render the XPS normally.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (const auto& s : System::IterateOver<Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(MultiplePagesType::BookFoldPrinting);
    }
}

// Once we print this document, we can turn it into a booklet by stacking the pages
// to come out of the printer and folding down the middle.
doc->Save(ArtifactsDir + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## See Also

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
