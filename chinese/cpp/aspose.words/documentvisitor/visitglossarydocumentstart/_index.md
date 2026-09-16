---
title: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart 方法"
linktitle: "VisitGlossaryDocumentStart"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart 方法。调用时，当在 C++ 中词汇表文档的枚举已开始。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words/documentvisitor/visitglossarydocumentstart/
---
## DocumentVisitor::VisitGlossaryDocumentStart method


当词汇表文档的枚举开始时调用。

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitGlossaryDocumentStart(System::SharedPtr<Aspose::Words::BuildingBlocks::GlossaryDocument> glossary)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 词汇表 | System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> | 正在被访问的对象。 |

### ReturnValue

一个指定如何继续枚举的 [VisitorAction](../../visitoraction/) 值。
## 备注


注意：在对 [Document](../../document/) 执行 Visitor 时，不会访问术语表文档节点及其子节点。如果想对术语表文档执行 Visitor，需要调用 [Accept()](../../../aspose.words.buildingblocks/glossarydocument/accept/)。

## 另见

* Enum [VisitorAction](../../visitoraction/)
* Class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
