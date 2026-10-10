---
title: "Aspose::Words::SubDocument::get_NodeType Methode"
linktitle: "get_NodeType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::SubDocument::get_NodeType Methode. Gibt SubDocument in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Gibt [SubDocument](../../nodetype/) zurück.

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Beispiele



Zeigt, wie auf das Subdokument eines Masterdokuments zugegriffen wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Dieser Knoten dient als Referenz zu einem externen Dokument, und sein Inhalt kann nicht abgerufen werden.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## Siehe auch

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
