---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageBorderAppliesTo enum. Spécifie sur quelles pages la bordure de page est imprimée en C++."
type: docs
weight: 106000
url: /fr/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Spécifie sur quelles pages la bordure de page est imprimée.

```cpp
enum class PageBorderAppliesTo
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| AllPages | 0 | La bordure de page est affichée sur toutes les pages de la section. |
| FirstPage | 1 | La bordure de page est affichée uniquement sur la première page de la section. |
| OtherPages | 2 | La bordure de page est affichée sur toutes les pages sauf la première page de la section. |


## Exemples



Montre comment créer une bordure à large bande bleue en haut de la première page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
