---
title: "Aspose::Words::Border::get_Shadow méthode"
linktitle: "get_Shadow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Border::get_Shadow méthode. Obtient ou définit une valeur indiquant si la bordure possède une ombre en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Obtient ou définit une valeur indiquant si la bordure a une ombre.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Remarques


Dans Microsoft Word, pour qu'une bordure possède une ombre, les bordures sur les quatre côtés (gauche, haut, droite et bas) doivent être du même type, largeur, couleur et toutes doivent avoir la propriété Shadow définie sur **true**.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
