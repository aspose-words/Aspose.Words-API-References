---
title: "Méthode Aspose::Words::Tables::Table::get_CellSpacing"
linktitle: "get_CellSpacing"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::Table::get_CellSpacing. Obtient ou définit la quantité d'espace (en points) entre les cellules en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words.tables/table/get_cellspacing/
---
## Table::get_CellSpacing method


Obtient ou définit la quantité d'espace (en points) entre les cellules.

```cpp
double Aspose::Words::Tables::Table::get_CellSpacing()
```


## Exemples



Montre comment activer l'espacement entre les cellules individuelles d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Définissez la propriété "AllowCellSpacing" sur "true" pour activer l'espacement entre les cellules
// avec une magnitude égale à la valeur de la propriété "CellSpacing", en points.
// Définissez la propriété "AllowCellSpacing" sur "false" pour désactiver l'espacement des cellules
// et ignorez la valeur de la propriété "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Modifier la propriété "CellSpacing" activera automatiquement l'espacement des cellules.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```


Montre comment créer des paramètres de style personnalisés pour le tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// La définition des propriétés de style d'un tableau peut affecter les propriétés du tableau lui‑même.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
