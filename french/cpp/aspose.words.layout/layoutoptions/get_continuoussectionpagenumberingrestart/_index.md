---
title: "Méthode Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart"
linktitle: "get_ContinuousSectionPageNumberingRestart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart. Obtient ou définit le mode de comportement pour le calcul des numéros de page lorsqu’une section continue redémarre la numérotation des pages en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Obtient ou définit le mode de comportement pour le calcul des numéros de page lorsqu'une section continue redémarre la numérotation des pages.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


## Exemples



Montre comment contrôler la numérotation des pages dans une section continue.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// Par défaut, le comportement d'Aspose.Words correspond à Microsoft Word 2019.
// Si vous avez besoin de l'ancien comportement d'Aspose.Words, similaire à Microsoft Word 2016, utilisez 'ContinuousSectionRestart.FromNewPageOnly'.
// La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où la section commence,
// à cause de cela, la numérotation sera réinitialisée à 2 à partir de la deuxième page.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## Voir aussi

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
