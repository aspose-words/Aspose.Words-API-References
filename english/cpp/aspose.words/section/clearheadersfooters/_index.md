---
title: Aspose::Words::Section::ClearHeadersFooters method
linktitle: ClearHeadersFooters
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section::ClearHeadersFooters method. Clears the headers and footers of this section in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


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
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->get_Count(), 0);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->get_Count(), 2);

ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->GetText().Trim(), u"This is the primary header.");
ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->GetText().Trim(), u"This is the primary footer.");

// Empty all the headers and footers in this section of all their contents.
// The headers and footers themselves will still be present but will have nothing to display.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->get_Count(), 2);

ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::HeaderPrimary)->GetText().Trim(), System::String::Empty);
ASSERT_EQ(doc->get_FirstSection()->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary)->GetText().Trim(), System::String::Empty);
```
## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


Clears the headers and footers of this section.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| Parameter | Type | Description |
| --- | --- | --- |
| preserveWatermarks | bool | True if the watermarks shall not be removed. |
## Remarks


The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.
## Examples


Shows how to clear the contents of header and footer with or without a watermark.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Header and footer types.docx"));

// Add a plain text watermark.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Make sure the headers and footers have content.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::HeaderFirst)->GetText().Trim(), u"First header");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::HeaderEven)->GetText().Trim(), u"Second header");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::HeaderPrimary)->GetText().Trim(), u"Third header");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::FooterFirst)->GetText().Trim(), u"First footer");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::FooterEven)->GetText().Trim(), u"Second footer");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::FooterPrimary)->GetText().Trim(), u"Third footer");

// Removes all header and footer content except watermarks.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::HeaderFirst)->GetText().Trim(), u"");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::HeaderEven)->GetText().Trim(), u"");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::HeaderPrimary)->GetText().Trim(), u"");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::FooterFirst)->GetText().Trim(), u"");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::FooterEven)->GetText().Trim(), u"");
ASSERT_EQ(headersFooters->idx_get(HeaderFooterType::FooterPrimary)->GetText().Trim(), u"");
ASSERT_EQ(doc->get_Watermark()->get_Type(), WatermarkType::Text);

// Removes all header and footer content including watermarks.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(doc->get_Watermark()->get_Type(), WatermarkType::None);
```
## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
