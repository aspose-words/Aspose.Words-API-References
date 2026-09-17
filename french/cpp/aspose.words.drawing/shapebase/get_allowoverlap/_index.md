---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap méthode"
linktitle: "get_AllowOverlap"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap méthode. Obtient ou définit une valeur qui spécifie si cette forme peut chevaucher d'autres formes en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Obtient ou définit une valeur qui indique si cette forme peut chevaucher d'autres formes.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Remarques


Cette propriété affecte le comportement de la forme dans Microsoft Word. Aspose.Words ignore la valeur de cette propriété.

Cette propriété ne s'applique qu'aux formes de niveau supérieur.

La valeur par défaut est **true**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
