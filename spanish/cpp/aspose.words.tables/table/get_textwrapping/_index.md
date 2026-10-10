---
title: "Aspose::Words::Tables::Table::get_TextWrapping método"
linktitle: "get_TextWrapping"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::get_TextWrapping método. Obtiene o establece TextWrapping para la tabla en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


Obtiene o establece [TextWrapping](./) para la tabla.

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## Ejemplos



Muestra cómo trabajar con el ajuste de texto de la tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Establece la propiedad "TextWrapping" a "TextWrapping.Around" para que la tabla envuelva el texto a su alrededor,
// y empújalo hacia abajo en el párrafo siguiente estableciendo la posición.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Ver también

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
