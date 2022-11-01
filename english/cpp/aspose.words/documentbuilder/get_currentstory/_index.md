---
title: get_CurrentStory
second_title: Aspose.Words for C++ API Reference
description: Gets the story that is currently selected in this DocumentBuilder.
type: docs
weight: 157
url: /cpp/aspose.words/documentbuilder/get_currentstory/
---
## DocumentBuilder.get_CurrentStory method


Gets the story that is currently selected in this [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::DocumentBuilder::get_CurrentStory()
```


## Examples




Shows how to work with a document builder's current story. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A Story is a type of node that has child Paragraph nodes, such as a Body.
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), doc->get_FirstSection()->get_Body());
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), builder->get_CurrentParagraph()->get_ParentNode());
ASSERT_EQ(StoryType::MainText, builder->get_CurrentStory()->get_StoryType());

builder->get_CurrentStory()->AppendParagraph(u"Text added to current Story.");

// A Story can also contain tables.
SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndTable();

ASSERT_TRUE(builder->get_CurrentStory()->get_Tables()->Contains(table));
```

