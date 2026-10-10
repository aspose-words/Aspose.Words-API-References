---
title: "Méthode Aspose::Words::Tables::CellFormat::get_PreferredWidth"
linktitle: "get_PreferredWidth"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::CellFormat::get_PreferredWidth. Retourne ou définit la largeur préférée de la cellule en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Renvoie ou définit la largeur préférée de la cellule.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Remarques


La largeur préférée (avec l'option Auto Fit du tableau) détermine comment la largeur réelle de la cellule est calculée par l'algorithme de mise en page du tableau. La mise en page du [Table](../../table/) peut être effectuée par Aspose.Words lors de l'enregistrement du document ou par Microsoft Word lors de l'affichage du document.

La largeur préférée peut être spécifiée en points ou en pourcentage. Elle peut également être spécifiée comme "auto", ce qui signifie qu'aucune largeur préférée n'est définie.

La valeur par défaut est [Auto](../../preferredwidth/auto/).

## Exemples



Montre comment définir une largeur préférée pour les cellules de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Il existe deux manières d'appliquer la classe "PreferredWidth" aux cellules de tableau.
// 1 -  Définir une largeur préférée absolue basée sur des points :
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Définir une largeur préférée relative basée sur le pourcentage de la largeur du tableau :
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Une cellule sans largeur préférée spécifiée occupera le reste de l'espace disponible.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Chaque configuration de la propriété "PreferredWidth" crée un nouvel objet.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Voir aussi

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
