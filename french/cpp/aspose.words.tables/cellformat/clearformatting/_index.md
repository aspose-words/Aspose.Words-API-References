---
title: "Méthode Aspose::Words::Tables::CellFormat::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::CellFormat::ClearFormatting. Réinitialise le format de cellule par défaut. Ne modifie pas la largeur de la cellule en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat::ClearFormatting method


Réinitialise la mise en forme par défaut de la cellule. Ne modifie pas la largeur de la cellule.

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
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

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
