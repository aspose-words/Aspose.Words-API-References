---
title: Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions method
linktitle: get_OutlineOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions method. Allows to specify outline options in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.saving/xpssaveoptions/get_outlineoptions/
---
## XpsSaveOptions::get_OutlineOptions method


Allows to specify outline options.

```cpp
System::SharedPtr<Aspose::Words::Saving::OutlineOptions> Aspose::Words::Saving::XpsSaveOptions::get_OutlineOptions() const
```

## Remarks


Note that [ExpandedOutlineLevels](../../outlineoptions/get_expandedoutlinelevels/) option will not work when saving to XPS.

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

* Class [OutlineOptions](../../outlineoptions/)
* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
