---
title: Aspose::Words::PageSetup::get_PaperSize method
linktitle: get_PaperSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_PaperSize method. Returns or sets the paper size in C++.'
type: docs
weight: 37000
url: /cpp/aspose.words/pagesetup/get_papersize/
---
## PageSetup::get_PaperSize method


Returns or sets the paper size.

```cpp
Aspose::Words::PaperSize Aspose::Words::PageSetup::get_PaperSize()
```

## Remarks


Setting this property updates [PageWidth](../get_pagewidth/) and [PageHeight](../get_pageheight/) values. Setting this value to [Custom](../../papersize/) does not change existing values.

## Examples



Shows how to adjust paper size, orientation, margins, along with other settings for a section. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Shows how to set page sizes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// We can change the current page's size to a pre-defined size
// by using the "PaperSize" property of this section's PageSetup object.
builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Tabloid);

ASPOSE_ASSERT_EQ(792.0, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(1224.0, builder->get_PageSetup()->get_PageHeight());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

// Each section has its own PageSetup object. When we use a document builder to make a new section,
// that section's PageSetup object inherits all the previous section's PageSetup object's values.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

ASSERT_EQ(Aspose::Words::PaperSize::Tabloid, builder->get_PageSetup()->get_PaperSize());

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::A5);
builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

ASPOSE_ASSERT_EQ(419.55, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(595.30, builder->get_PageSetup()->get_PageHeight());

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

// Set a custom size for this section's pages.
builder->get_PageSetup()->set_PageWidth(620);
builder->get_PageSetup()->set_PageHeight(480);

ASSERT_EQ(Aspose::Words::PaperSize::Custom, builder->get_PageSetup()->get_PaperSize());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

doc->Save(get_ArtifactsDir() + u"PageSetup.PaperSizes.docx");
```


Shows how to set the paper size of JisB4 or JisB5. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();
// Set the paper size to JisB4 (257x364mm).
pageSetup->set_PaperSize(Aspose::Words::PaperSize::JisB4);
// Alternatively, set the paper size to JisB5. (182x257mm).
pageSetup->set_PaperSize(Aspose::Words::PaperSize::JisB5);
```


Shows how to construct an Aspose.Words document by hand. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## See Also

* Enum [PaperSize](../../papersize/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
