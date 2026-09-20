---
title: "Aspose::Words::SubDocument::get_NodeType 方法"
linktitle: "get_NodeType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SubDocument::get_NodeType 方法。返回 SubDocument（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


返回 [SubDocument](../../nodetype/)。

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## 示例



展示如何访问主文档的子文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// 此节点用作对外部文档的引用，其内容无法访问。
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## 另见

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
