---
title: "Aspose::Words::CompositeNode::IndexOf 方法"
linktitle: "IndexOf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::IndexOf 方法。返回在 C++ 中子节点数组中指定子节点的索引。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/compositenode/indexof/
---
## CompositeNode::IndexOf method


返回指定子节点在子节点数组中的索引。

```cpp
int32_t Aspose::Words::CompositeNode::IndexOf(const System::SharedPtr<Aspose::Words::Node> &child)
```


## 示例



展示如何从父节点获取给定子节点的索引。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();

// 检索第一节正文中最后一个段落的索引。
ASSERT_EQ(24, body->GetChildNodes(Aspose::Words::NodeType::Any, false)->IndexOf(body->get_LastParagraph()));
```

## 另见

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
