---
title: "Método SetBorder de Aspose::Words::Tables::Table"
linktitle: "SetBorder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método SetBorder de Aspose::Words::Tables::Table. Establece el borde de tabla especificado al estilo de línea, ancho y color especificados en C++."
type: docs
weight: 68000
url: /es/cpp/aspose.words.tables/table/setborder/
---
## Table::SetBorder method


Establece el borde de tabla especificado al estilo de línea, ancho y color especificados.

```cpp
void Aspose::Words::Tables::Table::SetBorder(Aspose::Words::BorderType borderType, Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color, bool isOverrideCellBorders)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | El borde de tabla a cambiar. |
| lineStyle | Aspose::Words::LineStyle | El estilo de línea a aplicar. |
| lineWidth | double | El ancho de línea a establecer (en puntos). |
| color | System::Drawing::Color | El color a usar para el borde. |
| isOverrideCellBorders | bool | Cuando **true**, hace que todos los bordes de celda explícitos existentes se eliminen. |

## Ejemplos



Muestra cómo aplicar un borde de contorno a una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Alinea la tabla al centro de la página.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Elimina cualquier borde y sombreado existente de la tabla.
table->ClearBorders();
table->ClearShading();

// Añade bordes verdes al contorno de la tabla.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Rellena las celdas con un color sólido verde claro.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```

## Ver también

* Enum [BorderType](../../../aspose.words/bordertype/)
* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
