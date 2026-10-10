---
title: "Aspose::Words::SubDocument::get_NodeType méthode"
linktitle: "get_NodeType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::SubDocument::get_NodeType méthode. Retourne SubDocument en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/subdocument/get_nodetype/
---
## SubDocument::get_NodeType method


Retourne [SubDocument](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::SubDocument::get_NodeType() const override
```


## Exemples



Montre comment accéder au sous‑document d'un document principal.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// Ce nœud sert de référence à un document externe, et son contenu ne peut pas être consulté.
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## Voir aussi

* Enum [NodeType](../../nodetype/)
* Class [SubDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
