---
title: ClearContent
second_title: Aspose.Words for C++ API Reference
description: Clears the section.
type: docs
weight: 53
url: /cpp/aspose.words/section/clearcontent/
---
## Section::ClearContent method


Clears the section.

```cpp
void Aspose::Words::Section::ClearContent()
```

## Remarks


The text of [Body](../get_body/) is cleared, only one empty paragraph is left that represents the section break.

The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.

## Examples



Shows how to clear the contents of a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Running the "ClearContent" method will remove all the section contents
// but leave a blank paragraph to add content again.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
