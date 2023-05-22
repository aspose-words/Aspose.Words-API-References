---
title: Aspose::Words::Saving::OutlineOptions::get_HeadingsOutlineLevels method
linktitle: get_HeadingsOutlineLevels
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::OutlineOptions::get_HeadingsOutlineLevels method. Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/outlineoptions/get_headingsoutlinelevels/
---
## OutlineOptions::get_HeadingsOutlineLevels method


Specifies how many levels of headings (paragraphs formatted with the Heading styles) to include in the document outline.

```cpp
int32_t Aspose::Words::Saving::OutlineOptions::get_HeadingsOutlineLevels() const
```

## Remarks


Specify 0 for no headings in the outline; specify 1 for one level of headings in the outline and so on.

Default is 0. Valid range is 0 to 9.

## Examples



Shows how to convert a whole document to PDF with three levels in the document outline. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert headings of levels 1 to 5.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);

ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsHeading());

builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading2);

builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading3);

builder->Writeln(u"Heading 1.2.1");
builder->Writeln(u"Heading 1.2.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading4);

builder->Writeln(u"Heading 1.2.2.1");
builder->Writeln(u"Heading 1.2.2.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading5);

builder->Writeln(u"Heading 1.2.2.2.1");
builder->Writeln(u"Heading 1.2.2.2.2");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
// Clicking on an entry in this outline will take us to the location of its respective heading.
// Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
options->get_OutlineOptions()->set_HeadingsOutlineLevels(4);

// If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
// an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
// In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
// the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
// In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
// Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
// and collapse all level and 3 and higher entries when we open the document.
options->get_OutlineOptions()->set_ExpandedOutlineLevels(2);

doc->Save(ArtifactsDir + u"PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

## See Also

* Class [OutlineOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
