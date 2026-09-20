---
title: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes 方法"
linktitle: "GetChildNodes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes 方法。返回在 C++ 中匹配指定类型的子节点的实时集合。"
type: docs
weight: 34500
url: /zh/cpp/aspose.words.markup/structureddocumenttag/getchildnodes/
---
## StructuredDocumentTag::GetChildNodes method


返回匹配指定类型的子节点的实时集合。

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::Markup::StructuredDocumentTag::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | 指定要选择的节点类型。 |
| isDeep | bool | **true** 用于递归选择所有子节点；**false** 用于仅在直接子节点中选择。 |

### ReturnValue

指定类型的子节点的实时集合。
## 备注


此方法返回的节点集合始终是实时的。

实时集合始终与文档保持同步。例如，如果您选择文档中的所有章节并遍历集合删除这些章节，则当章节从文档中删除时，它会立即从集合中移除。

## 另见

* Class [NodeCollection](../../../aspose.words/nodecollection/)
* Enum [NodeType](../../../aspose.words/nodetype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
