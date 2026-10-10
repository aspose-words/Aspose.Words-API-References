---
title: "Aspose::Words::PageBorderDistanceFrom enum"
linktitle: "PageBorderDistanceFrom"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageBorderDistanceFrom enum. Spécifie le positionnement de la bordure de page par rapport à la marge de la page en C++."
type: docs
weight: 107000
url: /fr/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Spécifie le positionnement de la bordure de page par rapport à la marge de la page.

```cpp
enum class PageBorderDistanceFrom
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Text | 0 | La position de [Border](../border/) est mesurée à partir de la marge de la page. |
| PageEdge | 1 | La position de [Border](../border/) est mesurée à partir du bord de la page. |


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
