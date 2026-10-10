---
title: "Méthode Aspose::Words::ParagraphFormat::get_SnapToGrid"
linktitle: "get_SnapToGrid"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::ParagraphFormat::get_SnapToGrid. Indique si le paragraphe actuel doit utiliser les paramètres de lignes de grille du document par page lors de la mise en page du contenu du paragraphe en C++."
type: docs
weight: 30000
url: /fr/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Spécifie si le paragraphe actuel doit utiliser les paramètres de lignes de grille du document par page lors de la mise en page du contenu du paragraphe.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
