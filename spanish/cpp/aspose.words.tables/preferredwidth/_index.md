---
title: "Aspose::Words::Tables::PreferredWidth class"
linktitle: "PreferredWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::PreferredWidth class. Representa un valor y su unidad de medida que se utiliza para especificar el ancho preferido de una tabla o una celda. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Representa un valor y su unidad de medida que se usa para especificar el ancho preferido de una tabla o una celda. Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class PreferredWidth : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Auto](./auto/)() | Devuelve una instancia que representa el valor "el ancho preferido no está especificado". |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Determina si el [PreferredWidth](./) especificado es igual en valor al [PreferredWidth](./) actual. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina si el objeto especificado es igual en valor al objeto actual. |
| static [FromPercent](./frompercent/)(double) | Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado como un porcentaje. |
| static [FromPoints](./frompoints/)(double) | Un método de creación que devuelve una nueva instancia que representa un ancho preferido especificado usando un número de puntos. |
| [get_Type](./get_type/)() const | Obtiene la unidad de medida utilizada para este valor de ancho preferido. |
| [get_Value](./get_value/)() const | Obtiene el valor del ancho preferido. La unidad de medida se especifica en la propiedad [Type](./get_type/). |
| [GetHashCode](./gethashcode/)() const override | Sirve como función hash para este tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Devuelve una cadena fácil de usar que muestra el valor de este objeto. |
| static [Type](./type/)() |  |
## Observaciones


El ancho preferido puede especificarse como un porcentaje, número de puntos o un valor especial "none/auto".

Las instancias de esta clase son inmutables.

## Ejemplos



Muestra cómo ajustar una tabla automáticamente al 50% del ancho de la página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
