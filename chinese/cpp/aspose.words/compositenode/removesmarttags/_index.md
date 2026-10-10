---
title: "Aspose::Words::CompositeNode::RemoveSmartTags 方法"
linktitle: "RemoveSmartTags"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::RemoveSmartTags 方法。移除当前节点的所有 SmartTag 子孙节点（C++）。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words/compositenode/removesmarttags/
---
## CompositeNode::RemoveSmartTags method


移除当前节点的所有 [SmartTag](../../../aspose.words.markup/smarttag/) 子孙节点。

```cpp
void Aspose::Words::CompositeNode::RemoveSmartTags()
```


## 示例



从复合节点的子孙节点中移除所有智能标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

ASSERT_EQ(8, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());

doc->RemoveSmartTags();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->get_Count());
```

## 另见

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
