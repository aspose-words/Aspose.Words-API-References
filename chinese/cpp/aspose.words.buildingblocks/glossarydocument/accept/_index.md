---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept method"
linktitle: "Accept"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument::Accept method. 在 C++ 中接受访问者。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.buildingblocks/glossarydocument/accept/
---
## GlossaryDocument::Accept method


接受访问者。

```cpp
bool Aspose::Words::BuildingBlocks::GlossaryDocument::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 访问者 | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | 将访问这些节点的访问者。 |

### ReturnValue

如果所有节点都已被访问则为 True；如果 [DocumentVisitor](../../../aspose.words/documentvisitor/) 在访问所有节点之前停止了操作则为 false。
## 备注


遍历此节点及其所有子节点。每个节点都会调用 [DocumentVisitor](../../../aspose.words/documentvisitor/) 上的相应方法。

更多信息请参阅 Visitor 设计模式。

调用 [VisitGlossaryDocumentStart()](../../../aspose.words/documentvisitor/visitglossarydocumentstart/)，然后为该节点的所有子节点调用 [Accept()](../../../aspose.words/node/accept/)，最后调用 [VisitGlossaryDocumentEnd()](../../../aspose.words/documentvisitor/visitglossarydocumentend/)。

注意：当您对 [Document](../../../aspose.words/document/) 执行 Visitor 时，词汇文档节点及其子节点不会被访问。如果您想对词汇文档执行 Visitor，需要调用 [Accept()](./)。

## 另见

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [GlossaryDocument](../)
* Namespace [Aspose::Words::BuildingBlocks](../../)
* Library [Aspose.Words for C++](../../../)
