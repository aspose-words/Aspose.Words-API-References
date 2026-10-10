---
title: "Aspose::Words::Tables::PreferredWidth::get_Value méthode"
linktitle: "get_Value"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Value méthode. Obtient la valeur de la largeur préférée. L'unité de mesure est spécifiée dans la propriété Type en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Obtient la valeur de la largeur préférée. L'unité de mesure est spécifiée dans la propriété [Type](../get_type/).

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
