---
title: Aspose::Words::Tables::Table::get_CellSpacing method
linktitle: get_CellSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_CellSpacing method. Gets or sets the amount of space (in points) between the cells in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.tables/table/get_cellspacing/
---
## Table::get_CellSpacing method


Gets or sets the amount of space (in points) between the cells.

```cpp
double Aspose::Words::Tables::Table::get_CellSpacing()
```


## Examples



Shows how to enable spacing between individual cells in a table. 
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

// Set the "AllowCellSpacing" property to "true" to enable spacing between cells
// with a magnitude equal to the value of the "CellSpacing" property, in points.
// Set the "AllowCellSpacing" property to "false" to disable cell spacing
// and ignore the value of the "CellSpacing" property.
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Adjusting the "CellSpacing" property will automatically enable cell spacing.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```


Shows how to create custom style settings for the table. 
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
tableStyle->set_Bidi(true);
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

// Setting the style properties of a table may affect the properties of the table itself.
ASSERT_TRUE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
