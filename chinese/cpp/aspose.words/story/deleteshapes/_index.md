---
title: "Aspose::Words::Story::DeleteShapes 方法"
linktitle: "DeleteShapes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Story::DeleteShapes 方法。删除此故事文本中的所有形状（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


删除此故事文本中的所有形状。

```cpp
void Aspose::Words::Story::DeleteShapes()
```


## 示例



展示如何从节点中移除所有形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 DocumentBuilder 插入形状。这是一个内联形状，
// 它有一个父 Paragraph，该 Paragraph 是第一节 Body 的子节点。
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// 我们可以删除此 Body 的子段落中的所有形状。
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## 另见

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
