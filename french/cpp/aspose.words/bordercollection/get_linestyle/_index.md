---
title: "Aspose::Words::BorderCollection::get_LineStyle méthode"
linktitle: "get_LineStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_LineStyle méthode. Obtient ou définit le style de bordure en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Obtient ou définit le style de la bordure.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Remarques


Renvoie le style de la première bordure de la collection.

Définit le style de toutes les bordures de la collection, à l'exception des bordures diagonales.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
