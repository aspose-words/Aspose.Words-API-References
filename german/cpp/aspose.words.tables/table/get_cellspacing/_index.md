---
title: "Aspose::Words::Tables::Table::get_CellSpacing-Methode"
linktitle: "get_CellSpacing"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_CellSpacing-Methode. Ermittelt oder legt die Menge des Abstands (in Punkten) zwischen den Zellen in C++ fest."
type: docs
weight: 17000
url: /de/cpp/aspose.words.tables/table/get_cellspacing/
---
## Table::get_CellSpacing method


Ruft ab oder legt den Abstand (in Punkten) zwischen den Zellen fest.

```cpp
double Aspose::Words::Tables::Table::get_CellSpacing()
```


## Beispiele



Zeigt, wie man den Abstand zwischen einzelnen Zellen in einer Tabelle aktiviert.
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

// Setzen Sie die Eigenschaft "AllowCellSpacing" auf "true", um den Abstand zwischen Zellen zu aktivieren.
// mit einer Größe, die dem Wert der Eigenschaft "CellSpacing" entspricht, in Punkten.
// Setzen Sie die Eigenschaft "AllowCellSpacing" auf "false", um den Zellenabstand zu deaktivieren.
// und ignorieren Sie den Wert der Eigenschaft "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Das Anpassen der Eigenschaft "CellSpacing" aktiviert automatisch den Zellenabstand.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```


Zeigt, wie benutzerdefinierte Stileinstellungen für die Tabelle erstellt werden.
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

// Das Festlegen der Stil‑Eigenschaften einer Tabelle kann die Eigenschaften der Tabelle selbst beeinflussen.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
