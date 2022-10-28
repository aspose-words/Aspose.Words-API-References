---
title: HeaderFooter
second_title: Aspose.Words for C++ API Reference
description: Creates a new header or footer of the specified type.
type: docs
weight: 1
url: /cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter.HeaderFooter method


Creates a new header or footer of the specified type.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| headerFooterType | Aspose::Words::HeaderFooterType | A [HeaderFooterType](../get_headerfootertype/) value that specifies the type of the header or footer. |

When **HeaderFooter** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **HeaderFooter** to a **Section** use [Section.InsertAfter](../../compositenode/insertafter/), [Section.InsertBefore](../../compositenode/insertbefore/), HeadersFooters.Add or HeadersFooters.Insert.

## Examples




Shows how to create a header and a footer. 
```cpp
auto doc = MakeObject<Document>();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
auto header = MakeObject<HeaderFooter>(doc, HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

SharedPtr<Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
auto footer = MakeObject<HeaderFooter>(doc, HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(ArtifactsDir + u"HeaderFooter.Create.docx");
```

