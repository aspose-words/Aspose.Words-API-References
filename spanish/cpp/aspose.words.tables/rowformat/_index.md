---
title: "Aspose::Words::Tables::RowFormat class"
linktitle: "RowFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::RowFormat class. Representa todo el formato de una fila de tabla. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


Representa todo el formato de una fila de tabla. Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Restablece el formato de fila predeterminado. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Verdadero si se permite que el texto en una fila de tabla se divida en un salto de página. |
| [get_Borders](./get_borders/)() | Obtiene la colección de bordes de celda predeterminados para la fila. |
| [get_HeadingFormat](./get_headingformat/)() | Verdadero si la fila se repite como encabezado de tabla en cada página cuando la tabla abarca más de una página. |
| [get_Height](./get_height/)() | Obtiene o establece la altura de la fila de tabla en puntos. |
| [get_HeightRule](./get_heightrule/)() | Obtiene o establece la regla para determinar la altura de la fila de tabla. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Establecedor para [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | Establecedor para [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | Método setter para [Aspose::Words::Tables::RowFormat::get_Height](./get_height/). |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | Método setter para [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo crear una tabla con bordes personalizados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Configuración de opciones de formato de tabla para un DocumentBuilder
// se aplicarán a cada fila y celda que añadamos con él.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Cambiar el formato lo aplicará a la celda actual,
// y a cualquier celda nueva que creemos con el constructor posteriormente.
// Esto no afectará a las celdas que hemos añadido previamente.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Aumenta la altura de la fila para ajustar el texto vertical.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Muestra cómo modificar el formato de filas y celdas en una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Utilice la propiedad "RowFormat" de la primera fila para modificar el formato
// del contenido de todas las celdas de esta fila.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Utilice la propiedad "CellFormat" de la primera celda en la última fila para modificar el formato del contenido de esa celda.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Muestra cómo modificar el formato de una fila de tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Utilice la propiedad "RowFormat" de la primera fila para establecer un formato que modifique la apariencia completa de esa fila.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## Ver también

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
