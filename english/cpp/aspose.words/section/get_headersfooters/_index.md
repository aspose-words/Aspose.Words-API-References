---
title: get_HeadersFooters
second_title: Aspose.Words for C++ API Reference
description: Provides access to the headers and footers nodes of the section.
type: docs
weight: 131
url: /cpp/aspose.words/section/get_headersfooters/
---
## Section::get_HeadersFooters method


Provides access to the headers and footers nodes of the section.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooterCollection> Aspose::Words::Section::get_HeadersFooters()
```


## Examples



Shows how to delete all footers from a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Header and footer types.docx");

// Iterate through each section and remove footers of every kind.
for (const auto& section : System::IterateOver(doc->LINQ_OfType<SharedPtr<Section>>()))
{
    // There are three kinds of footer and header types.
    // 1 -  The "First" header/footer, which only appears on the first page of a section.
    SharedPtr<HeaderFooter> footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterFirst);
    if (footer != nullptr)
    {
        footer->Remove();
    }

    // 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary);
    if (footer != nullptr)
    {
        footer->Remove();
    }

    // 3 -  The "Even" header/footer, which appears on even pages.
    footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterEven);
    if (footer != nullptr)
    {
        footer->Remove();
    }

    ASSERT_EQ(0,
              section->get_HeadersFooters()->LINQ_Count([](SharedPtr<Node> hf) { return !(System::DynamicCast<HeaderFooter>(hf))->get_IsHeader(); }));
}

doc->Save(ArtifactsDir + u"HeaderFooter.RemoveFooters.docx");
```


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

## See Also

* Class [HeaderFooterCollection](../../headerfootercollection/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
