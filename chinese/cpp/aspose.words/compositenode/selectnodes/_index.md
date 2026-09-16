---
title: "Aspose::Words::CompositeNode::SelectNodes 方法"
linktitle: "SelectNodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CompositeNode::SelectNodes 方法。选择在 C++ 中匹配 XPath 表达式的节点列表。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words/compositenode/selectnodes/
---
## CompositeNode::SelectNodes method


选择匹配 XPath 表达式的节点列表。

```cpp
System::SharedPtr<Aspose::Words::NodeList> Aspose::Words::CompositeNode::SelectNodes(const System::String &xpath)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| xpath | const System::String\& | XPath 表达式。 |

### ReturnValue

匹配 XPath 查询的节点列表。
## 备注


目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

## 另见

* Class [NodeList](../../nodelist/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
