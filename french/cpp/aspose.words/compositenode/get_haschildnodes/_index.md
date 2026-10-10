---
title: "Aspose::Words::CompositeNode::get_HasChildNodes méthode"
linktitle: "get_HasChildNodes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::get_HasChildNodes méthode. Retourne true si ce nœud possède des nœuds enfants en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode::get_HasChildNodes method


Renvoie **true** si ce nœud possède des nœuds enfants.

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## Exemples



Montre comment combiner les lignes de deux tables en une seule.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Voici deux façons d'obtenir une table à partir d'un document.
// 1 -  À partir de la collection "Tables" d'un nœud Body :
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  En utilisant la méthode "GetChild" :
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Ajoutez toutes les lignes de la table actuelle à la suivante.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Supprimez le conteneur de table vide.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Voir aussi

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
