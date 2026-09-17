---
title: "Aspose::Words::Tables::PreferredWidth::GetHashCode méthode"
linktitle: "GetHashCode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::PreferredWidth::GetHashCode méthode. Sert de fonction de hachage pour ce type en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.tables/preferredwidth/gethashcode/
---
## PreferredWidth::GetHashCode method


Servit de fonction de hachage pour ce type.

```cpp
int32_t Aspose::Words::Tables::PreferredWidth::GetHashCode() const override
```


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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
