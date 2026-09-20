---
title: "Aspose::Words::Tables::Table::get_Style método"
linktitle: "get_Style"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::get_Style método. Obtiene o establece el estilo de tabla aplicado a esta tabla en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words.tables/table/get_style/
---
## Table::get_Style method


Obtiene o establece el estilo de tabla aplicado a esta tabla.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Tables::Table::get_Style()
```


## Ejemplos



Muestra cómo crear configuraciones de estilo personalizadas para la tabla.
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

// Establecer las propiedades de estilo de una tabla puede afectar las propiedades de la propia tabla.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Ver también

* Class [Style](../../../aspose.words/style/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
