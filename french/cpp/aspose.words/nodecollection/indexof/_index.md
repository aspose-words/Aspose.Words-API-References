---
title: "Méthode Aspose::Words::NodeCollection::IndexOf"
linktitle: "IndexOf"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::NodeCollection::IndexOf. Retourne l'index basé sur zéro du nœud spécifié en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Renvoie l'index basé sur zéro du nœud spécifié.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nœud | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à localiser. |

### ReturnValue

L'index basé sur zéro du nœud dans la collection, s'il est trouvé ; sinon, -1.
## Remarques


Cette méthode effectue une recherche linéaire ; par conséquent, le temps d'exécution moyen est proportionnel à [Count](../get_count/).

## Exemples



Montre comment obtenir l'index d'un nœud dans une collection.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## Voir aussi

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
