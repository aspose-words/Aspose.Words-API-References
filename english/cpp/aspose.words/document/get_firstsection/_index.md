---
title: Aspose::Words::Document::get_FirstSection method
linktitle: get_FirstSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_FirstSection method. Gets the first section in the document in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words/document/get_firstsection/
---
## Document::get_FirstSection method


Gets the first section in the document.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Document::get_FirstSection()
```


## Examples



Shows how to replace text in a document's footer. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


Shows how to create a new section with a document builder. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A blank document contains one section by default,
// which contains child nodes that we can edit.
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Use a document builder to add text to the first section.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Create a second section by inserting a section break.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(2, doc->get_Sections()->get_Count());

// Each section has its own page setup settings.
// We can split the text in the second section into two columns.
// This will not affect the text in the first section.
doc->get_LastSection()->get_PageSetup()->get_TextColumns()->SetCount(2);
builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

ASSERT_EQ(1, doc->get_FirstSection()->get_PageSetup()->get_TextColumns()->get_Count());
ASSERT_EQ(2, doc->get_LastSection()->get_PageSetup()->get_TextColumns()->get_Count());

doc->Save(get_ArtifactsDir() + u"Section.Create.docx");
```


Shows how to iterate through the children of a composite node. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

System::SharedPtr<Aspose::Words::Section> section = doc->get_FirstSection();

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
for (auto&& node : System::IterateOver(section))
{
    switch (node->get_NodeType())
    {
        case Aspose::Words::NodeType::Body:
            {
                auto body = System::ExplicitCast<Aspose::Words::Body>(node);

                std::cout << "Body:" << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", body->GetText().Trim()) << std::endl;
                break;
            }

        case Aspose::Words::NodeType::HeaderFooter:
            {
                auto headerFooter = System::ExplicitCast<Aspose::Words::HeaderFooter>(node);

                std::cout << System::String::Format(u"HeaderFooter type: {0}:", headerFooter->get_HeaderFooterType()) << std::endl;
                std::cout << System::String::Format(u"\t\"{0}\"", headerFooter->GetText().Trim()) << std::endl;
                break;
            }

        default:
            {
                throw System::Exception(u"Unexpected node type in a section.");
            }

    }
}
```

## See Also

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
