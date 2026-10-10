---
title: "Aspose::Words::CompositeNode::SelectSingleNode 方法"
linktitle: "SelectSingleNode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::SelectSingleNode 方法。选择在 C++ 中匹配 XPath 表达式的第一个 Node。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode::SelectSingleNode method


选择匹配 XPath 表达式的第一个 [Node](../../node/)。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::SelectSingleNode(const System::String &xpath)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xpath | const System::String\& | XPath 表达式。 |

### ReturnValue

匹配 XPath 查询的第一个 [Node](../../node/)；如果未找到匹配的节点，则为 **null**。
## 备注


目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

## 另见

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
