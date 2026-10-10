---
title: "Aspose::Words::Tables::PreferredWidth::get_Type méthode"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Type méthode. Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
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

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
