---
title: "Méthode Aspose::Words::Tables::Table::get_AllowOverlap"
linktitle: "get_AllowOverlap"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::get_AllowOverlap. Indique si un tableau flottant doit autoriser d'autres objets flottants dans le document à chevaucher ses limites lors de l'affichage. La valeur par défaut est true en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Obtient si un tableau flottant doit permettre à d'autres objets flottants dans le document de chevaucher ses limites lorsqu'il est affiché. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
