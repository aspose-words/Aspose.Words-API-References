---
title: "Aspose::Words::DocumentBuilder::DeleteRow méthode"
linktitle: "DeleteRow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::DeleteRow méthode. Supprime une ligne d'un tableau en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Supprime une ligne d'un tableau.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| tableIndex | int32_t | L'index de la table. |
| rowIndex | int32_t | L'index de la ligne dans le tableau. |

### ReturnValue

Le nœud de ligne qui vient d'être supprimé.
## Remarques


Si le curseur se trouve à l'intérieur de la ligne qui est en cours de suppression, le curseur est déplacé vers la ligne suivante ou vers le paragraphe suivant après la table.

Si vous supprimez une ligne d'une table qui ne contient qu'une seule ligne, toute la table est supprimée.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il indique un index à partir du début, 0 étant le premier élément. Lorsque l'index est inférieur à 0, il indique un index depuis la fin, -1 étant le dernier élément.

## Exemples



Montre comment supprimer une ligne d'une table.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Supprimez la première ligne de la première table du document.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## Voir aussi

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
