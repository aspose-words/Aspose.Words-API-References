---
title: "Méthode Aspose::Words::PageSetup::get_LayoutMode"
linktitle: "get_LayoutMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_LayoutMode méthode. Obtient ou définit le mode de mise en page de cette section en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words/pagesetup/get_layoutmode/
---
## PageSetup::get_LayoutMode method


Obtient ou définit le mode de mise en page de cette section.

```cpp
Aspose::Words::SectionLayoutMode Aspose::Words::PageSetup::get_LayoutMode()
```


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

* Enum [SectionLayoutMode](../../sectionlayoutmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
