---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing método"
linktitle: "get_AllowCellSpacing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing método. Obtiene o establece la opción \"Permitir espacio entre celdas\" en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


Obtiene o establece la opción "Allow spacing between cells".

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Ejemplos



Muestra cómo habilitar el espacio entre celdas individuales en una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Establezca la propiedad "AllowCellSpacing" a "true" para habilitar el espacio entre celdas
// con una magnitud igual al valor de la propiedad "CellSpacing", en puntos.
// Establezca la propiedad "AllowCellSpacing" a "false" para desactivar el espacio entre celdas
// e ignore el valor de la propiedad "CellSpacing".
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// Ajustar la propiedad "CellSpacing" habilitará automáticamente el espacio entre celdas.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
