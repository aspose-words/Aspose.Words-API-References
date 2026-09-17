---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::PreferredWidthType enum. Spécifie l'unité de mesure de la largeur préférée d'une table ou d'une cellule en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Spécifie l'unité de mesure de la largeur préférée d'un tableau ou d'une cellule.

```cpp
enum class PreferredWidthType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Auto | 1 | La largeur préférée n'est pas spécifiée. La largeur réelle de la table ou de la cellule est soit spécifiée à l'aide de la largeur explicite, soit déterminée automatiquement par l'algorithme de mise en page de la table lors de l'affichage de la table, en fonction du paramètre d'ajustement automatique de la table. |
| Percent | 2 | Mesurez la largeur actuelle de l'élément en utilisant un pourcentage spécifié. |
| Points | 3 | Mesurez la largeur actuelle de l'élément en utilisant un nombre spécifié de points (1/72 pouce). |


## Exemples



Montre comment vérifier le type et la valeur de la largeur préférée d'une cellule de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Voir aussi

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
