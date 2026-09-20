---
title: "Método get_StyleIdentifier de Aspose::Words::Tables::Table"
linktitle: "get_StyleIdentifier"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_StyleIdentifier de Aspose::Words::Tables::Table. Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words.tables/table/get_styleidentifier/
---
## Table::get_StyleIdentifier method


Obtiene o establece el identificador de estilo independiente de la configuración regional del estilo de tabla aplicado a esta tabla.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Tables::Table::get_StyleIdentifier()
```


## Ejemplos



Muestra cómo crear una tabla nueva mientras se aplica un estilo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Debemos insertar al menos una fila antes de aplicar cualquier formato de tabla.
builder->InsertCell();

// Establezca el estilo de tabla usado según el identificador de estilo.
// Tenga en cuenta que no todos los estilos de tabla están disponibles al guardar en formato .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Aplique parcialmente el estilo a las características de la tabla según los predicados, luego construya la tabla.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## Ver también

* Enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
