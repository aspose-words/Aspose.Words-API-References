---
title: Aspose::Words::DocumentBuilder::get_CurrentStory method
linktitle: get_CurrentStory
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::get_CurrentStory method. Gets the story that is currently selected in this DocumentBuilder in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words/documentbuilder/get_currentstory/
---
## DocumentBuilder::get_CurrentStory method


Gets the story that is currently selected in this [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::DocumentBuilder::get_CurrentStory()
```


## Examples



Shows how to work with a document builder's current story. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A Story is a type of node that has child Paragraph nodes, such as a Body.
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), doc->get_FirstSection()->get_Body());
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), builder->get_CurrentParagraph()->get_ParentNode());
ASSERT_EQ(Aspose::Words::StoryType::MainText, builder->get_CurrentStory()->get_StoryType());

builder->get_CurrentStory()->AppendParagraph(u"Text added to current Story.");

// A Story can also contain tables.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndTable();

ASSERT_TRUE(builder->get_CurrentStory()->get_Tables()->Contains(table));
```

## See Also

* Class [Story](../../story/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
