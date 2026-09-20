---
title: "Método Aspose::Words::TableStyle::get_TopPadding"
linktitle: "get_TopPadding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::TableStyle::get_TopPadding. Obtiene o establece la cantidad de espacio (en puntos) que se agrega encima del contenido de las celdas de tabla en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words/tablestyle/get_toppadding/
---
## TableStyle::get_TopPadding method


Obtiene o establece la cantidad de espacio (en puntos) que se agrega encima del contenido de las celdas de la tabla.

```cpp
double Aspose::Words::TableStyle::get_TopPadding()
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

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
