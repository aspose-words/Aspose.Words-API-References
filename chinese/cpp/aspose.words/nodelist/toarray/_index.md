---
title: "Aspose::Words::NodeList::ToArray 方法"
linktitle: "ToArray"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeList::ToArray 方法。将集合中的所有节点复制到一个新的节点数组中（C++）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/nodelist/toarray/
---
## NodeList::ToArray method


将集合中的所有节点复制到一个新的节点数组中。

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeList::ToArray() const
```


### ReturnValue

一个节点数组。
## 备注


在遍历节点集合时不应添加/删除节点，因为这会使迭代器失效，并且需要为实时集合刷新。

若需在迭代期间添加/删除节点，请使用此方法将节点复制到固定大小的数组中，然后遍历该数组。

## 另见

* Class [Node](../../node/)
* Class [NodeList](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
