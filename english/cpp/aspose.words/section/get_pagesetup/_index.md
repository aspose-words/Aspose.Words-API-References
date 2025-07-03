---
title: Aspose::Words::Section::get_PageSetup method
linktitle: get_PageSetup
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section::get_PageSetup method. Returns an object that represents page setup and section properties in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/section/get_pagesetup/
---
## Section::get_PageSetup method


Returns an object that represents page setup and section properties.

```cpp
System::SharedPtr<Aspose::Words::PageSetup> Aspose::Words::Section::get_PageSetup()
```


## Examples



Shows how to create a wide blue band border at the top of the first page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
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

* Class [PageSetup](../../pagesetup/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
