---
title: "Aspose::Words::PageSetup::get_CharactersPerLine méthode"
linktitle: "get_CharactersPerLine"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_CharactersPerLine méthode. Obtient ou définit le nombre de caractères par ligne dans la grille du document en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Obtient ou définit le nombre de caractères par ligne dans la grille du document.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Remarques


La valeur minimale de la propriété est 1. La valeur maximale dépend de la largeur de la page et de la taille de police du style Normal. Le pas de caractère minimal est de 90 % de la taille de la police. Par exemple, le nombre maximal de caractères par ligne d’une page Letter avec des marges d’un pouce est de 43.

Par défaut, la propriété possède une valeur pour laquelle le pas de caractère est égal à la taille de police du style Normal.

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

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
