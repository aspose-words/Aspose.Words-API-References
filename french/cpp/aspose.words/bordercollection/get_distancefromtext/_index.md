---
title: "Aspose::Words::BorderCollection::get_DistanceFromText méthode"
linktitle: "get_DistanceFromText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::BorderCollection::get_DistanceFromText méthode. Obtient ou définit la distance de la bordure par rapport au texte en points en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Obtient ou définit la distance de la bordure par rapport au texte en points.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Remarques


Obtient la distance du texte pour la première bordure.

Définit la distance du texte pour toutes les bordures de la collection, à l'exception des bordures diagonales.

N'a aucun effet et sera automatiquement réinitialisé à zéro pour les bordures des cellules de tableau.

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
