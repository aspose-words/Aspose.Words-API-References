---
title: "Aspose::Words::Layout::ContinuousSectionRestart enum"
linktitle: "ContinuousSectionRestart"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::ContinuousSectionRestart enum. Représente différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Représente différents comportements lors du calcul des numéros de page dans une section continue qui redémarre la numérotation des pages.

```cpp
enum class ContinuousSectionRestart
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Toujours | 0 | La numérotation des pages redémarre toujours, quel que soit le flux de contenu. |
| FromNewPageOnly | 1 | La numérotation des pages redémarre uniquement s'il n'y a aucun autre contenu avant la section sur la page où la section commence. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
