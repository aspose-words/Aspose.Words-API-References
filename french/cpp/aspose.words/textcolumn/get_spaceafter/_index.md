---
title: "Méthode Aspose::Words::TextColumn::get_SpaceAfter"
linktitle: "get_SpaceAfter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::TextColumn::get_SpaceAfter. Obtient ou définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/textcolumn/get_spaceafter/
---
## TextColumn::get_SpaceAfter method


Obtient ou définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne.

```cpp
double Aspose::Words::TextColumn::get_SpaceAfter()
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

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
