---
title: "Aspose::Words::Tables::PreferredWidth class"
linktitle: "PreferredWidth"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::PreferredWidth class. Représente une valeur et son unité de mesure utilisées pour spécifier la largeur préférée d'une table ou d'une cellule. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Représente une valeur et son unité de mesure utilisées pour spécifier la largeur préférée d’un tableau ou d’une cellule. Pour en savoir plus, consultez l’article de documentation [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class PreferredWidth : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Auto](./auto/)() | Renvoie une instance qui représente la valeur "la largeur préférée n'est pas spécifiée". |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Détermine si le [PreferredWidth](./) spécifié est égal en valeur au [PreferredWidth](./) actuel. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| static [FromPercent](./frompercent/)(double) | Une méthode de création qui renvoie une nouvelle instance représentant une largeur préférée spécifiée en pourcentage. |
| static [FromPoints](./frompoints/)(double) | Une méthode de création qui renvoie une nouvelle instance représentant une largeur préférée spécifiée à l'aide d'un nombre de points. |
| [get_Type](./get_type/)() const | Obtient l'unité de mesure utilisée pour cette valeur de largeur préférée. |
| [get_Value](./get_value/)() const | Obtient la valeur de la largeur préférée. L'unité de mesure est spécifiée dans la propriété [Type](./get_type/). |
| [GetHashCode](./gethashcode/)() const override | Servit de fonction de hachage pour ce type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |
| static [Type](./type/)() |  |
## Remarques


La largeur préférée peut être spécifiée en pourcentage, en nombre de points ou une valeur spéciale "none/auto".

Les instances de cette classe sont immuables.

## Exemples



Montre comment régler une table pour qu'elle s'ajuste automatiquement à 50 % de la largeur de la page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
