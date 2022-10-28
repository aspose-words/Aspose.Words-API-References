---
title: get_CreateMissingOutlineLevels
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to create missing outline levels when the document is exported. Default value for this property is false.
type: docs
weight: 27
url: /cpp/aspose.words.saving/outlineoptions/get_createmissingoutlinelevels/
---
## OutlineOptions.get_CreateMissingOutlineLevels method


Gets or sets a value determining whether or not to create missing outline levels when the document is exported. Default value for this property is **false**.

```cpp
bool Aspose::Words::Saving::OutlineOptions::get_CreateMissingOutlineLevels() const
```


## Examples




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

