---
title: SectionStart
second_title: Aspose.Words for C++ API Reference
description: The type of break at the beginning of the section.
type: docs
weight: 1496
url: /cpp/aspose.words/sectionstart/
---
## SectionStart enum


The type of break at the beginning of the section.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Continuous | 0 | The new section starts on the same page as the previous section. |
| NewColumn | 1 | The section starts from a new column. |
| NewPage | 2 | The section starts from a new page. |
| EvenPage | 3 | The section starts on a new even page. |
| OddPage | 4 | The section starts on a new odd page. |


## Examples




Shows how to specify how a new section separates itself from the previous. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// Section break types determine how a new section separates itself from the previous section.
// Below are five types of section breaks.
// 1 -  Starts the next section on a new page:
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(SectionStart::NewPage, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());

// 2 -  Starts the next section on the current page:
builder->InsertBreak(BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(SectionStart::Continuous, doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart());

// 3 -  Starts the next section on a new even page:
builder->InsertBreak(BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(SectionStart::EvenPage, doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart());

// 4 -  Starts the next section on a new odd page:
builder->InsertBreak(BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(SectionStart::OddPage, doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart());

// 5 -  Starts the next section on a new column:
SharedPtr<TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(SectionStart::NewColumn, doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart());

doc->Save(ArtifactsDir + u"PageSetup.SetSectionStart.docx");
```


Shows how to construct an Aspose.Words document by hand. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = MakeObject<Section>(doc);
doc->AppendChild(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = MakeObject<Body>(doc);
section->AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = MakeObject<Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

body->AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = MakeObject<Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(ArtifactsDir + u"Section.CreateManually.docx");
```

