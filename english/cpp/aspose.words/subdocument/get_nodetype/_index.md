---
title: Aspose::Words::SubDocument::get_NodeType method
linktitle: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::SubDocument::get_NodeType method. Returns SubDocument in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Returns [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Examples



Shows how to access a master document's subdocument. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// This node serves as a reference to an external document, and its contents cannot be accessed.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## See Also

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
