---
title: Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions constructor
linktitle: XpsSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions constructor. Initializes a new instance of this class that can be used to save a document in the Xps format in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions::XpsSaveOptions() constructor


Initializes a new instance of this class that can be used to save a document in the [Xps](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions()
```


## Examples



Shows how to limit the headings' level that will appear in the outline of a saved XPS document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert headings that can serve as TOC entries of levels 1, 2, and then 3.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

// Create an "XpsSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
auto saveOptions = MakeObject<XpsSaveOptions>();

ASSERT_EQ(SaveFormat::Xps, saveOptions->get_SaveFormat());

// The output XPS document will contain an outline, a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(ArtifactsDir + u"XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

## See Also

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat) constructor


Initializes a new instance of this class that can be used to save a document in the [Xps](../../../aspose.words/saveformat/) or [OpenXps](../../../aspose.words/saveformat/) format.

```cpp
Aspose::Words::Saving::XpsSaveOptions::XpsSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
