---
title: "Aspose::Words::TableStyle::get_Alignment método"
linktitle: "get_Alignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TableStyle::get_Alignment método. Especifica la alineación para el estilo de tabla en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/tablestyle/get_alignment/
---
## TableStyle::get_Alignment method


Especifica la alineación para el estilo de tabla.

```cpp
Aspose::Words::Tables::TableAlignment Aspose::Words::TableStyle::get_Alignment()
```


## Ejemplos



Muestra cómo establecer la posición de una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de alinear una tabla horizontalmente.
// 1 -  Utilice la propiedad "Alignment" para alinearla a una ubicación en la página, como el centro:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Inserte una tabla y aplique el estilo que creamos a ella.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Utilice la "LeftIndent" para especificar una sangría desde el margen izquierdo de la página:
tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(get_ArtifactsDir() + u"Table.SetTableAlignment.docx");
```

## Ver también

* Enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
