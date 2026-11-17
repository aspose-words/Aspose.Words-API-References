---
title: Aspose::Words::Section::ClearContent method
linktitle: ClearContent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section::ClearContent method. Clears the section in C++.'
type: docs
weight: 5000
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Running the "ClearContent" method will remove all the section contents
// but leave a blank paragraph to add content again.
doc->get_FirstSection()->ClearContent();

ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
```

## See Also

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
