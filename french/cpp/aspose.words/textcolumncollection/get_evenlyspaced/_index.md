---
title: "Méthode Aspose::Words::TextColumnCollection::get_EvenlySpaced"
linktitle: "get_EvenlySpaced"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::TextColumnCollection::get_EvenlySpaced. Vrai si les colonnes de texte ont la même largeur et sont espacées uniformément en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/textcolumncollection/get_evenlyspaced/
---
## TextColumnCollection::get_EvenlySpaced method


Vrai si les colonnes de texte ont une largeur égale et sont espacées uniformément.

```cpp
bool Aspose::Words::TextColumnCollection::get_EvenlySpaced()
```


## Exemples



Montre comment créer des colonnes à espacement irrégulier.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Déterminez la quantité d'espace dont nous disposons pour organiser les colonnes.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Définissez la première colonne comme étroite.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Définissez la deuxième colonne pour qu'elle occupe le reste de l'espace disponible à l'intérieur des marges de la page.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Voir aussi

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
