---
title: get_IsHeading
second_title: Aspose.Words for C++ API Reference
description: True when the paragraph style is one of the built-in Heading styles.
type: docs
weight: 170
url: /cpp/aspose.words/paragraphformat/get_isheading/
---
## ParagraphFormat.get_IsHeading method


True when the paragraph style is one of the built-in Heading styles.

```cpp
bool Aspose::Words::ParagraphFormat::get_IsHeading()
```


## Examples




Shows how to limit the headings' level that will appear in the outline of a saved PDF document. 
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

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Pdf);

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "2" to exclude all headings whose levels are above 2 from the outline.
// The last two headings we have inserted above will not appear.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(2);

doc->Save(ArtifactsDir + u"PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

