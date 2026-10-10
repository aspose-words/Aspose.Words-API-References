---
title: "Aspose::Words::Tables::Table::get_CellSpacing metodo"
linktitle: "get_CellSpacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::get_CellSpacing metodo. Ottiene o imposta la quantità di spazio (in punti) tra le celle in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.tables/table/get_cellspacing/
---
## Table::get_CellSpacing method


Ottiene o imposta la quantità di spazio (in punti) tra le celle.

```cpp
double Aspose::Words::Tables::Table::get_CellSpacing()
```


## Esempi



Mostra come abilitare la spaziatura tra le singole celle in una tabella.
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

// Imposta la proprietà \"AllowCellSpacing\" su \"true\" per abilitare la spaziatura tra le celle
// con una magnitudine pari al valore della proprietà \"CellSpacing\", in punti.
// Imposta la proprietà \"AllowCellSpacing\" su \"false\" per disabilitare la spaziatura tra le celle
// e ignora il valore della proprietà \"CellSpacing\".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Regolare la proprietà \"CellSpacing\" abiliterà automaticamente la spaziatura tra le celle.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```


Mostra come creare impostazioni di stile personalizzate per la tabella.
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

// Impostare le proprietà di stile di una tabella può influire sulle proprietà della stessa tabella.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
