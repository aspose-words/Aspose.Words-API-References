---
title: "Aspose::Words::PageSetup::get_Borders méthode"
linktitle: "get_Borders"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_Borders méthode. Obtient une collection des bordures de page en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup::get_Borders method


Obtient une collection des bordures de page.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


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

* Class [BorderCollection](../../bordercollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
