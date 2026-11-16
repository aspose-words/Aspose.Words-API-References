---
title: Aspose::Words::Document::get_Sections method
linktitle: get_Sections
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_Sections method. Returns a collection that represents all sections in the document in C++.'
type: docs
weight: 140000
url: /cpp/aspose.words/document/get_sections/
---
## Document::get_Sections method


Returns a collection that represents all sections in the document.

```cpp
System::SharedPtr<Aspose::Words::SectionCollection> Aspose::Words::Document::get_Sections()
```

## Examples


Shows how to specify how a new section separates itself from the previous.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"This text is in section 1.");

// Section break types determine how a new section separates itself from the previous section.
// Below are five types of section breaks.
// 1 -  Starts the next section on a new page:
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Writeln(u"This text is in section 2.");

ASSERT_EQ(doc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart(), SectionStart::NewPage);

// 2 -  Starts the next section on the current page:
builder->InsertBreak(BreakType::SectionBreakContinuous);
builder->Writeln(u"This text is in section 3.");

ASSERT_EQ(doc->get_Sections()->idx_get(2)->get_PageSetup()->get_SectionStart(), SectionStart::Continuous);

// 3 -  Starts the next section on a new even page:
builder->InsertBreak(BreakType::SectionBreakEvenPage);
builder->Writeln(u"This text is in section 4.");

ASSERT_EQ(doc->get_Sections()->idx_get(3)->get_PageSetup()->get_SectionStart(), SectionStart::EvenPage);

// 4 -  Starts the next section on a new odd page:
builder->InsertBreak(BreakType::SectionBreakOddPage);
builder->Writeln(u"This text is in section 5.");

ASSERT_EQ(doc->get_Sections()->idx_get(4)->get_PageSetup()->get_SectionStart(), SectionStart::OddPage);

// 5 -  Starts the next section on a new column:
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->SetCount(2);

builder->InsertBreak(BreakType::SectionBreakNewColumn);
builder->Writeln(u"This text is in section 6.");

ASSERT_EQ(doc->get_Sections()->idx_get(5)->get_PageSetup()->get_SectionStart(), SectionStart::NewColumn);

doc->Save(get_ArtifactsDir() + u"PageSetup.SetSectionStart.docx");
```

Shows how to add and remove sections in a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(doc->GetText().Trim(), u"Section 1\x000c" u"Section 2");

// Delete the first section from the document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(doc->GetText().Trim(), u"Section 2");

// Append a copy of what is now the first section to the end of the document.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(doc->GetText().Trim(), u"Section 2\x000c" u"Section 2");
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
