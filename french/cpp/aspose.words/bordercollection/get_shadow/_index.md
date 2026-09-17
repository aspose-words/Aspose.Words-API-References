---
title: "Aspose::Words::BorderCollection::get_Shadow méthode"
linktitle: "get_Shadow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_Shadow méthode. Obtient ou définit une valeur indiquant si la bordure a une ombre en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Obtient ou définit une valeur indiquant si la bordure a une ombre.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Remarques


Obtient la valeur de la première bordure de la collection.

Définit la valeur pour toutes les bordures de la collection, à l'exception des bordures diagonales.

## Exemples



Montre comment créer une bordure de page verte ondulée avec une ombre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## Voir aussi

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
