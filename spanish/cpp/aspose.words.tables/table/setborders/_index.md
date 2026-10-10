---
title: "Aspose::Words::Tables::Table::SetBorders método"
linktitle: "SetBorders"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::SetBorders método. Establece todos los bordes de la tabla al estilo de línea, ancho y color especificados en C++."
type: docs
weight: 69000
url: /es/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Establece todos los bordes de la tabla al estilo de línea, ancho y color especificados.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | El estilo de línea a aplicar. |
| lineWidth | double | El ancho de línea a establecer (en puntos). |
| color | System::Drawing::Color | El color a usar para el borde. |

## Ejemplos



Muestra cómo aplicar el color de borde y sombreado al crear una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inicia una tabla y establece un color/grosor predeterminado para sus bordes.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Crea una fila con dos celdas con diferentes colores de fondo.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Restablece el formato de la celda para desactivar los colores de fondo
// establece un grosor de borde personalizado para todas las celdas nuevas creadas por el generador,
// luego construye una segunda fila.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Muestra cómo formatear todos los bordes de una tabla a la vez.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Elimina todos los bordes existentes de la tabla.
table->ClearBorders();

// Establece una única línea verde para servir como cada borde externo e interno de esta tabla.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## Ver también

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
