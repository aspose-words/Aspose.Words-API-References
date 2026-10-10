---
title: "Aspose::Words::NodeList::idx_get 方法"
linktitle: "idx_get"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeList::idx_get 方法。检索给定索引处的节点（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/nodelist/idx_get/
---
## NodeList::idx_get method


检索给定索引处的节点。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeList::idx_get(int32_t index) const
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 节点列表中的索引。 |
## 备注


索引从零开始。

允许使用负索引，并表示从集合的末尾访问。例如 -1 表示最后一个项目，-2 表示倒数第二个，依此类推。

如果索引大于或等于列表中的项目数，则返回空引用。

如果索引为负且其绝对值大于列表中的项目数，则返回空引用。

## 另见

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
