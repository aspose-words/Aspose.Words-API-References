---
title: Aspose::Words::DocumentBuilder::InsertHtml method
linktitle: InsertHtml
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertHtml method. Inserts an HTML string into the document in C++.'
type: docs
weight: 37000
url: /cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


Inserts an HTML string into the document.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| Parameter | Type | Description |
| --- | --- | --- |
| html | const System::String\& | An HTML string to insert into the document. |

## Examples



Shows how to use a document builder to insert html content into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// Inserting HTML code parses the formatting of each element into equivalent document text formatting.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


Inserts an HTML string into the document. Allows to specify additional options.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| Parameter | Type | Description |
| --- | --- | --- |
| html | const System::String\& | An HTML string to insert into the document. |
| options | Aspose::Words::HtmlInsertOptions | Options that are used when HTML string is inserted. |

## See Also

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


Inserts an HTML string into the document.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| Parameter | Type | Description |
| --- | --- | --- |
| html | const System::String\& | An HTML string to insert into the document. |
| useBuilderFormatting | bool | A value indicating whether formatting specified in [DocumentBuilder](../) is used as base formatting for text imported from HTML. |
## Remarks


You can use this method to insert an HTML fragment or whole HTML document.

When *useBuilderFormatting* is **false**, [DocumentBuilder](../) formating is ignored and formatting of inserted text is based on default HTML formatting. As a result, the text looks as it is rendered in browsers.

When *useBuilderFormatting* is **true**, formatting of inserted text is based on [DocumentBuilder](../) formatting, and the text looks as if it were inserted with [Write()](../).

## Examples



Shows how to apply a document builder's formatting while inserting HTML content. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
// the paragraph alignment value found in the HTML code always supersedes the document builder's value.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// The second paragraph has no alignment specified. It can have its alignment value filled in
// by the builder's value depending on the flag we passed to the InsertHtml method.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## See Also

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
