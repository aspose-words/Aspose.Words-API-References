---
title: Aspose::Words::HeaderFooterCollection::LinkToPrevious method
linktitle: LinkToPrevious
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeaderFooterCollection::LinkToPrevious method. Links or unlinks the specified header or footer to the corresponding header or footer in the previous section in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


Links or unlinks the specified header or footer to the corresponding header or footer in the previous section.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | A [HeaderFooterType](../../headerfootertype/) value that specifies the header or footer to link/unlink. |
| isLinkToPrevious | bool | **true** to link the header or footer to the previous section; **false** to unlink. |
## Remarks


If the header or footer of the specified type does not exist, creates it automatically.

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

## See Also

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


Links or unlinks all headers and footers to the corresponding headers and footers in the previous section.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| Parameter | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** to link the headers and footers to the previous section; **false** to unlink them. |
## Remarks


If any of the headers or footers do not exist, creates them automatically.

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

## See Also

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
