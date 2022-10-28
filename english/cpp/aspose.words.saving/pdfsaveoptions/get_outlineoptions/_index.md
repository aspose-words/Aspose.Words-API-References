---
title: get_OutlineOptions
second_title: Aspose.Words for C++ API Reference
description: Allows to specify outline options.
type: docs
weight: 287
url: /cpp/aspose.words.saving/pdfsaveoptions/get_outlineoptions/
---
## PdfSaveOptions.get_OutlineOptions method


Allows to specify outline options.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::PdfSaveOptions::get_OutlineOptions() const
```


Outlines can be created from headings and bookmarks.

For headings outline level is determined by the heading level.

It is possible to set the max heading level to be included into outlines or disable heading outlines at all.

For bookmarks outline level may be set in options as a default value for all bookmarks or as individual values for particular bookmarks.

Also, outlines can be exported to XPS format by using the same [OutlineOptions](./) class.

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


Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert headings that can serve as TOC entries of levels 1 and 5.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading5);

builder->Writeln(u"Heading 1.1.1.1.1");
builder->Writeln(u"Heading 1.1.1.1.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "5" to include all headings of levels 5 and below in the outline.
saveOptions->get_OutlineOptions()->set_HeadingsOutlineLevels(5);

// This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
// The output PDF document will treat outline levels 2, 3, and 4 as "missing".
// Set the "CreateMissingOutlineLevels" property to "true" to include all missing levels in the outline,
// leaving blank outline entries since there are no usable headings.
// Set the "CreateMissingOutlineLevels" property to "false" to ignore missing outline levels,
// and treat the outline level 5 headings as level 2.
saveOptions->get_OutlineOptions()->set_CreateMissingOutlineLevels(createMissingOutlineLevels);

doc->Save(ArtifactsDir + u"PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

