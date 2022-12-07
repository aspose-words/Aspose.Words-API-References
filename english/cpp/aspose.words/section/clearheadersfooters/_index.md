---
title: ClearHeadersFooters
second_title: Aspose.Words for C++ API Reference
description: Clears the headers and footers of this section.
type: docs
weight: 66
url: /cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters method


Clears the headers and footers of this section.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## Remarks


The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.

## Examples



Shows how to clear the contents of all headers and footers in a section. 
```cpp
auto doc = MakeObject<Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = MakeObject<DocumentBuilder>(doc);

builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->GetText().Trim());

// Empty all the headers and footers in this section of all their contents.
// The headers and footers themselves will still be present but will have nothing to display.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
