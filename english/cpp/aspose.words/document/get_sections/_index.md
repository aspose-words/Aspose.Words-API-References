---
title: Aspose::Words::Document::get_Sections method
linktitle: get_Sections
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_Sections method. Returns a collection that represents all sections in the document in C++.'
type: docs
weight: 48000
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


Shows how to add and remove sections in a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c"
          u"Section 2",
          doc->GetText().Trim());

// Delete the first section from the document.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Append a copy of what is now the first section to the end of the document.
int lastSectionIdx = doc->get_Sections()->get_Count() - 1;
SharedPtr<Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c"
          u"Section 2",
          doc->GetText().Trim());
```

## See Also

* Class [SectionCollection](../../sectioncollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
