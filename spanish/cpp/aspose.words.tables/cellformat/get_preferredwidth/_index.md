---
title: "Método Aspose::Words::Tables::CellFormat::get_PreferredWidth"
linktitle: "get_PreferredWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::CellFormat::get_PreferredWidth. Devuelve o establece el ancho preferido de la celda en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Devuelve o establece el ancho preferido de la celda.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Observaciones


El ancho preferido (junto con la opción Auto Fit de la tabla) determina cómo el ancho real de la celda es calculado por el algoritmo de diseño de la tabla. El diseño de [Table](../../table/) puede ser realizado por Aspose.Words al guardar el documento o por Microsoft Word al mostrar el documento.

El ancho preferido puede especificarse en puntos o en porcentaje. El ancho preferido también puede especificarse como "auto", lo que significa que no se especifica un ancho preferido.

El valor predeterminado es [Auto](../../preferredwidth/auto/).

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

## Ver también

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
