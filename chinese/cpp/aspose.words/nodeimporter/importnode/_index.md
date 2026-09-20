---
title: "Aspose::Words::NodeImporter::ImportNode 方法"
linktitle: "ImportNode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeImporter::ImportNode 方法。将一个文档中的节点导入到另一个文档中，使用 C++。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/nodeimporter/importnode/
---
## NodeImporter::ImportNode method


将节点从一个文档导入到另一个文档中。

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::NodeImporter::ImportNode(const System::SharedPtr<Aspose::Words::Node> &srcNode, bool isImportChildren)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | const System::SharedPtr\<Aspose::Words::Node\>\& | 要导入的节点。 |
| isImportChildren | bool | **true** 表示递归导入所有子节点；否则为 **false**。 |

### ReturnValue

已克隆并导入的节点。该节点属于目标文档，但没有父节点。
## 备注


导入节点会创建一个属于导入文档的源节点的副本。返回的节点没有父节点。源节点不会被修改或从原始文档中移除。

在将另一个文档的节点插入此文档之前，必须先导入它。导入期间，文档特定的属性（如样式和列表的引用）会从原始文档转换到导入文档。节点导入后，可使用 [InsertBefore1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertAfter</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertAfter1()](../) 将其插入文档的适当位置。

如果源节点已经属于目标文档，则仅创建该源节点的深度克隆。

## 另见

* Class [Node](../../node/)
* Class [NodeImporter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
