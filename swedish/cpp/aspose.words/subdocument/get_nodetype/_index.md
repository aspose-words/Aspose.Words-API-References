---
title: "Aspose::Words::SubDocument::get_NodeType-metoden"
linktitle: "get_NodeType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::SubDocument::get_NodeType-metoden. Returnerar SubDocument i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Returnerar [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Exempel



Visar hur man får åtkomst till ett huvuddokuments subdokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Denna nod fungerar som en referens till ett externt dokument, och dess innehåll kan inte nås.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## Se även

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
