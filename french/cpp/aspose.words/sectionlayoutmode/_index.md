---
title: "Aspose::Words::SectionLayoutMode énumération"
linktitle: "SectionLayoutMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::SectionLayoutMode énumération. Spécifie le mode de mise en page d'une section permettant de définir le comportement de la grille du document en C++."
type: docs
weight: 115000
url: /fr/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Spécifie le mode de mise en page d'une section permettant de définir le comportement de la grille du document.

```cpp
enum class SectionLayoutMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Default | 0 | Spécifie qu'aucune grille de document ne doit être appliquée au contenu de la section correspondante dans le document. |
| Grille | 1 | Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et chaque caractère qu'elle contient afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. Les caractères ne seront pas automatiquement alignés sur les lignes de la grille lors de la saisie. |
| LineGrid | 2 | Spécifie que la section correspondante doit avoir un pas de ligne supplémentaire ajouté à chaque ligne qu'elle contient afin de maintenir le nombre spécifié de lignes par page. |
| SnapToChars | 3 | Spécifie que la section correspondante doit avoir à la fois le pas de ligne supplémentaire et le pas de caractère ajoutés à chaque ligne et chaque caractère qu'elle contient afin de maintenir un nombre spécifique de lignes par page et de caractères par ligne. Les caractères seront automatiquement alignés sur les lignes de la grille lors de la saisie. |


## Exemples



Montre comment spécifier une limite pour le nombre de caractères que chaque ligne peut contenir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Activez le crénage, puis utilisez-le pour définir le nombre de caractères par ligne dans cette section.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Le nombre de caractères dépend également de la taille de la police.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
