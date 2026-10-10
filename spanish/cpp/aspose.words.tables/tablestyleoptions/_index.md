---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::TableStyleOptions enum. Especifica cómo se aplica el estilo de tabla a una tabla en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Especifica cómo se aplica el estilo de tabla a una tabla.

```cpp
enum class TableStyleOptions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se aplica formato de estilo de tabla. |
| FirstRow | 32 | Aplicar formato condicional a la primera fila. |
| LastRow | 64 | Aplicar formato condicional a la última fila. |
| FirstColumn | 128 | Aplicar formato condicional a la primera columna 1. |
| LastColumn | 256 | Aplicar formato condicional a la última columna. |
| RowBands | 512 | Aplicar formato condicional de bandas de fila. |
| ColumnBands | 1024 | Aplicar formato condicional de bandas de columna. |
| Default2003 | n/a | [Row](../row/) y se aplican bandas de columna. Este es el valor predeterminado de Microsoft Word para formatos antiguos como DOC, WML y RTF. |
| Predeterminado | n/a | Estos son los valores predeterminados de Microsoft Word. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
