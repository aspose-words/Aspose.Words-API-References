---
title: "Aspose::Words::PageSetup::get_LinesPerPage méthode"
linktitle: "get_LinesPerPage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_LinesPerPage méthode. Obtient ou définit le nombre de lignes par page dans la grille du document en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Obtient ou définit le nombre de lignes par page dans la grille du document.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Remarques


La valeur minimale de la propriété est 1. La valeur maximale dépend de la hauteur de la page et de la taille de police du style Normal. Le pas de ligne minimal est de 136 % de la taille de police. Par exemple, le nombre maximal de lignes par page d’une page Letter avec des marges d’un pouce est de 39.

Par défaut, la propriété a une valeur pour laquelle le pas de ligne est 1,5 fois supérieur à la taille de police du style Normal.

## Exemples



Montre comment spécifier une limite pour le nombre de lignes que chaque page peut contenir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Activez le crénage, puis utilisez-le pour définir le nombre de lignes par page dans cette section.
// Une taille de police suffisamment grande repoussera certaines lignes vers la page suivante afin d'éviter le chevauchement des caractères.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
