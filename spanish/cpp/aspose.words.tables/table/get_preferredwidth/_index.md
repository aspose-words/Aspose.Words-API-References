---
title: "Método Aspose::Words::Tables::Table::get_PreferredWidth"
linktitle: "get_PreferredWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::get_PreferredWidth. Obtiene o establece el ancho preferido de la tabla en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Obtiene o establece el ancho preferido de la tabla.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Observaciones


El valor predeterminado es [Auto](../../preferredwidth/auto/).

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

## Ver también

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
