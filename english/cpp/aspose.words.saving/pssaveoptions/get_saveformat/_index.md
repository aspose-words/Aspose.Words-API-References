---
title: Aspose::Words::Saving::PsSaveOptions::get_SaveFormat method
linktitle: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PsSaveOptions::get_SaveFormat method. Specifies the format in which the document will be saved if this save options object is used. Can only be Ps in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


Specifies the format in which the document will be saved if this save options object is used. Can only be [Ps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


## Examples



Shows how to save a document to the Postscript format in the form of a book fold. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// Create a "PsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to PostScript.
// Set the "UseBookFoldPrintingSettings" property to "true" to arrange the contents
// in the output Postscript document in a way that helps us make a booklet out of it.
// Set the "UseBookFoldPrintingSettings" property to "false" to save the document normally.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// If we are rendering the document as a booklet, we must set the "MultiplePages"
// properties of the page setup objects of all sections to "MultiplePagesType.BookFoldPrinting".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// Once we print this document on both sides of the pages, we can fold all the pages down the middle at once,
// and the contents will line up in a way that creates a booklet.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## See Also

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
