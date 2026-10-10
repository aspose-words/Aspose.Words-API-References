---
title: "Aspose::Words::Tables::CellCollection classe"
linktitle: "CellCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::CellCollection classe. Fournit un accès typé à une collection de nœuds Cell. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.tables/cellcollection/
---
## CellCollection class


Fournit un accès typé à une collection de nœuds [Cell](../cell/). Pour en savoir plus, consultez l'article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellCollection : public Aspose::Words::NodeCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Détermine si un nœud se trouve dans la collection. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Obtient le nombre de nœuds dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Récupère un [Cell](../cell/) à l'index donné. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](./toarray/)() | Copie toutes les cellules de la collection dans un nouveau tableau de cellules. |
| static [Type](./type/)() |  |

## Exemples



Montre comment parcourir toutes les tables du document et imprimer le contenu de chaque cellule.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Nous pouvons utiliser la méthode "ToArray" sur une collection de lignes pour la cloner dans un tableau.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Nous pouvons utiliser la méthode "ToArray" sur une collection de cellules pour la cloner dans un tableau.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## Voir aussi

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
