---
title: "Méthode Aspose::Words::Border::get_DistanceFromText"
linktitle: "get_DistanceFromText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Border::get_DistanceFromText. Obtient ou définit la distance de la bordure par rapport au texte ou au bord de la page en points en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/border/get_distancefromtext/
---
## Border::get_DistanceFromText method


Obtient ou définit la distance de la bordure par rapport au texte ou au bord de la page en points.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
```


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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
