---
title: "Metodo Aspose::Words::SubDocument::get_NodeType"
linktitle: "get_NodeType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::SubDocument::get_NodeType. Restituisce SubDocument in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Restituisce [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Esempi



Mostra come accedere al subdocumento di un documento master.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Questo nodo funge da riferimento a un documento esterno e il suo contenuto non può essere accessibile.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## Vedi anche

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
