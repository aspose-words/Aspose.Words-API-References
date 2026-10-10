---
title: "Método Aspose::Words::Tables::Table::get_AllowAutoFit"
linktitle: "get_AllowAutoFit"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::get_AllowAutoFit. Permite que Microsoft Word y Aspose.Words redimensionen automáticamente las celdas de una tabla para que se ajusten a su contenido en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Permite que Microsoft Word y Aspose.Words redimensionen automáticamente las celdas de una tabla para ajustarse a su contenido.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Observaciones


El valor predeterminado es **true**.

## Ejemplos



Muestra cómo habilitar/deshabilitar el redimensionamiento automático de celdas de tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Establezca la propiedad "AllowAutoFit" a "false" para que la tabla mantenga las dimensiones
// de todas sus filas y celdas, y trunque el contenido si se vuelve demasiado grande para ajustarse.
// Establezca la propiedad "AllowAutoFit" a "true" para permitir que la tabla cambie el ancho y la altura de sus celdas
// para acomodar su contenido.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
