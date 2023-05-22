---
title: Aspose::Words::Document::get_LastSection method
linktitle: get_LastSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_LastSection method. Gets the last section in the document in C++.'
type: docs
weight: 35000
url: /cpp/aspose.words/document/get_lastsection/
---
## Document::get_LastSection method


Gets the last section in the document.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_LastSection()
```


## Examples



Shows how to create a new section with a document builder. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains one section by default,
// which contains child nodes that we can edit.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Use a document builder to add text to the first section.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a second section by inserting a section break.
builder->InsertBreak(BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Each section has its own page setup settings.
// We can split the text in the second section into two columns.
// This will not affect the text in the first section.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(ArtifactsDir + u"Section.Create.docx");
```

## See Also

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
