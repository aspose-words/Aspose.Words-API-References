---
title: Aspose::Words::Paragraph::get_ParentStory method
linktitle: get_ParentStory
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_ParentStory method. Retrieves the parent section-level story that can be Body or HeaderFooter in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words/paragraph/get_parentstory/
---
## Paragraph::get_ParentStory method


Retrieves the parent section-level story that can be [Body](../../body/) or [HeaderFooter](../../headerfooter/).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::Paragraph::get_ParentStory()
```


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

## See Also

* Class [Story](../../story/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
