---
title: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: Returns NodeType.SubDocument
type: docs
weight: 14
url: /cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument.get_NodeType method


Returns **NodeType.SubDocument**

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Examples




Shows how to access a master document's subdocument. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Master document.docx");

SharedPtr<NodeCollection> subDocuments = doc->GetChildNodes(NodeType::SubDocument, true);

// This node serves as a reference to an external document, and its contents cannot be accessed.
auto subDocument = System::DynamicCast<SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

