---
title: get_FirstSection
second_title: Aspose.Words for C++ API Reference
description: Gets the first section in the document.
type: docs
weight: 300
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
auto doc = MakeObject<Document>(MyDir + u"Footer.docx");

SharedPtr<HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
SharedPtr<HeaderFooter> footer = headersFooters->idx_get(HeaderFooterType::FooterPrimary);

auto options = MakeObject<FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(ArtifactsDir + u"HeaderFooter.ReplaceText.docx");
```


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


Shows how to iterate through the children of a composite node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Write(u"Primary header");
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Write(u"Primary footer");

SharedPtr<Section> section = doc->get_FirstSection();

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
for (const auto& node : System::IterateOver(section))
{
    switch (node->get_NodeType())
    {
    case NodeType::Body: {
        auto body = System::DynamicCast<Body>(node);

        std::cout << "Body:" << std::endl;
        std::cout << "\t\"" << body->GetText().Trim() << "\"" << std::endl;
        break;
    }

    case NodeType::HeaderFooter: {
        auto headerFooter = System::DynamicCast<HeaderFooter>(node);

        std::cout << String::Format(u"HeaderFooter type: {0}:", headerFooter->get_HeaderFooterType()) << std::endl;
        std::cout << "\t\"" << headerFooter->GetText().Trim() << "\"" << std::endl;
        break;
    }

    default: {
        throw System::Exception(u"Unexpected node type in a section.");
    }
    }
}
```

## See Also

* Class [Section](../../section/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
