---
title: "Aspose::Words::Tables::Cell::Cell 构造函数"
linktitle: "单元格"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Cell::Cell 构造函数。初始化 Cell 类的新实例（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.tables/cell/cell/
---
## Cell::Cell constructor


初始化 [Cell](../) 类的新实例。

```cpp
Aspose::Words::Tables::Cell::Cell(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
## 备注


当创建 [Cell](../) 时，它属于指定的文档，但尚未成为文档的一部分，并且 [ParentNode](../../../aspose.words/node/get_parentnode/) 为 **null**。

要将 [Cell](../) 追加到文档中，请在希望插入单元格的行上使用 [InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../)。

## 另见

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
