---
title: "Aspose::Words::NodeCollection::Clear méthode"
linktitle: "Clear"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeCollection::Clear méthode. Supprime tous les nœuds de cette collection et du document en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Supprime tous les nœuds de cette collection et du document.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Exemples



Montre comment supprimer toutes les sections d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Ce document possède une section avec quelques nœuds enfants contenant et affichant tout le contenu du document.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Effacez la collection de sections, ce qui supprimera tous les enfants du document.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## Voir aussi

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
