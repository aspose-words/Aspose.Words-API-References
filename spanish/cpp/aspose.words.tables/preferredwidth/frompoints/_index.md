---
title: "Aspose::Words::Tables::PreferredWidth::FromPoints método"
linktitle: "FromPoints"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::PreferredWidth::FromPoints método. Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado usando un número de puntos en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth::FromPoints method


Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado usando un número de puntos.

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::PreferredWidth::FromPoints(double points)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| puntos | double | El valor debe estar entre 0 y 22 pulgadas (22 * 72 puntos). |

## Ejemplos



Muestra cómo establecer un ancho preferido para las celdas de la tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Hay dos formas de aplicar la clase "PreferredWidth" a las celdas de la tabla.
// 1 -  Establezca un ancho preferido absoluto basado en puntos:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Establezca un ancho preferido relativo basado en el porcentaje del ancho de la tabla:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Una celda sin ancho preferido especificado ocupará el resto del espacio disponible.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Cada configuración de la propiedad "PreferredWidth" crea un nuevo objeto.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```


Muestra cómo usar herramientas de conversión de unidades al especificar un ancho preferido para una celda.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(Aspose::Words::ConvertUtil::InchToPoint(3)));
builder->InsertCell();

ASPOSE_ASSERT_EQ(216.0, table->get_FirstRow()->get_FirstCell()->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Ver también

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
