---
title: "Aspose::Words::Markup::SmartTag::SmartTag 构造函数"
linktitle: "SmartTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SmartTag::SmartTag 构造函数. 在 C++ 中初始化 SmartTag 类的新实例."
type: docs
weight: 2000
url: /zh/cpp/aspose.words.markup/smarttag/smarttag/
---
## SmartTag::SmartTag constructor


初始化 [SmartTag](../) 类的新实例.

```cpp
Aspose::Words::Markup::SmartTag::SmartTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
## 备注


当您创建新节点时，需要指定该节点所属的文档. 节点不能在没有文档的情况下存在，因为它依赖于文档范围的结构，如列表和样式. 虽然节点始终属于文档，但节点可能是也可能不是文档树的一部分.

当创建节点时，它属于文档，但尚未成为文档树的一部分，且 [ParentNode](../../../aspose.words/node/get_parentnode/) 为 null. 要将节点插入文档，请在父节点上使用 [InsertAfter1()</see> 或 <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) 方法.

## 另见

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [SmartTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
