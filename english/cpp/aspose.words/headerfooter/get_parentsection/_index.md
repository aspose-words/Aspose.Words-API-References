---
title: Aspose::Words::HeaderFooter::get_ParentSection method
linktitle: get_ParentSection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeaderFooter::get_ParentSection method. Gets the parent section of this story in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/headerfooter/get_parentsection/
---
## HeaderFooter::get_ParentSection method


Gets the parent section of this story.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::HeaderFooter::get_ParentSection()
```

## Remarks


[ParentSection](./) is equivalent to [ParentNode](../../node/get_parentnode/) casted to [Section](../../section/).

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
                 [](SharedPtr<Node> hf) { return !(System::ExplicitCast<HeaderFooter>(hf))->get_IsLinkedToPrevious(); }));

// All the second section's header/footers are linked to the first section's headers/footers.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(
                 [](SharedPtr<Node> hf) { return (System::ExplicitCast<HeaderFooter>(hf))->get_IsLinkedToPrevious(); }));

// In the third section, only the footer is linked to the first section's footer via the second section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(
                 [](SharedPtr<Node> hf) { return !(System::ExplicitCast<HeaderFooter>(hf))->get_IsLinkedToPrevious(); }));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(ArtifactsDir + u"HeaderFooter.Link.docx");
```

## See Also

* Class [Section](../../section/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
