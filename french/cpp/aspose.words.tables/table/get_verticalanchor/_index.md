---
title: "Aspose::Words::Tables::Table::get_VerticalAnchor méthode"
linktitle: "get_VerticalAnchor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::get_VerticalAnchor méthode. Obtient l'objet de base à partir duquel le positionnement vertical du tableau flottant doit être calculé. La valeur par défaut est Margin en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Obtient l'objet de base à partir duquel le positionnement vertical du tableau flottant doit être calculé. La valeur par défaut est [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
```


## Exemples



Montre comment travailler avec les propriétés des tableaux flottants.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Seuls Margin, Page, Column sont disponibles dans RelativeHorizontalPosition pour le définisseur HorizontalAnchor.
    // L'ArgumentException sera levée pour toute autre valeur.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Seuls Margin, Page, Paragraph sont disponibles dans RelativeVerticalPosition pour le définisseur VerticalAnchor.
    // L'ArgumentException sera levée pour toute autre valeur.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Voir aussi

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
