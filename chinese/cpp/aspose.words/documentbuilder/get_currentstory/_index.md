---
title: "Aspose::Words::DocumentBuilder::get_CurrentStory 方法"
linktitle: "get_CurrentStory"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::get_CurrentStory 方法。 在 C++ 中获取此 DocumentBuilder 当前选中的 Story。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/documentbuilder/get_currentstory/
---
## DocumentBuilder::get_CurrentStory method


获取此 [DocumentBuilder](../) 当前选中的 Story。

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::DocumentBuilder::get_CurrentStory()
```


## 示例



展示如何使用文档构建器的当前 Story。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Story 是一种节点类型，拥有子 Paragraph 节点，例如 Body。
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), doc->get_FirstSection()->get_Body());
ASPOSE_ASSERT_EQ(builder->get_CurrentStory(), builder->get_CurrentParagraph()->get_ParentNode());
ASSERT_EQ(Aspose::Words::StoryType::MainText, builder->get_CurrentStory()->get_StoryType());

builder->get_CurrentStory()->AppendParagraph(u"Text added to current Story.");

// Story 还可以包含表格。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1");
builder->InsertCell();
builder->Write(u"Row 1, cell 2");
builder->EndTable();

ASSERT_TRUE(builder->get_CurrentStory()->get_Tables()->Contains(table));
```

## 另见

* Class [Story](../../story/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
