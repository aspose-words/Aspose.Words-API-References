---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Retrieves a HeaderFooter of the specified type.
type: docs
weight: 1
url: /cpp/aspose.words/headerfootercollection/idx_get/
---
## HeaderFooterCollection.idx_get(Aspose::Words::HeaderFooterType) method


Retrieves a **HeaderFooter** of the specified type.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | A [HeaderFooterType](../../headerfootertype/) value that specifies the type of the header/footer to retrieve. |

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

## HeaderFooterCollection.idx_get(int32_t) method


Retrieves a **HeaderFooter** at the given index.

```cpp
System::SharedPtr<Aspose::Words::HeaderFooter> Aspose::Words::HeaderFooterCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

## Examples




Shows how to link headers and footers between sections. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// Move to the first section and create a header and a footer. By default,
// the header and the footer will only appear on pages in the section that contains them.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// We can link a section's headers/footers to the previous section's headers/footers
// to allow the linking section to display the linked section's headers/footers.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Each section will still have its own header/footer objects. When we link sections,
// the linking section will display the linked section's header/footers while keeping its own.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(),
                 doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Link the headers/footers of the third section to the headers/footers of the second section.
// The second section already links to the first section's header/footers,
// so linking to the second section will create a link chain.
// The first, second, and now the third sections will all display the first section's headers.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// We can also select only a specific type of header/footer to link using this method.
// The third section now will have the same footer as the second and first sections, but not the header.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(HeaderFooterType::FooterPrimary, true);

// The first section's header/footers cannot link themselves to anything because there is no previous section.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(
                 [](SharedPtr<Node> hf) { return !(System::DynamicCast<HeaderFooter>(hf))->get_IsLinkedToPrevious(); }));

// All the second section's header/footers are linked to the first section's headers/footers.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(
                 [](SharedPtr<Node> hf) { return (System::DynamicCast<HeaderFooter>(hf))->get_IsLinkedToPrevious(); }));

// In the third section, only the footer is linked to the first section's footer via the second section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(
                 [](SharedPtr<Node> hf) { return !(System::DynamicCast<HeaderFooter>(hf))->get_IsLinkedToPrevious(); }));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(ArtifactsDir + u"HeaderFooter.Link.docx");
```

