---
title: "Aspose::Words::Tables::Table::AutoFit método"
linktitle: "AutoFit"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::AutoFit método. Cambia el tamaño de la tabla y las celdas según el comportamiento de ajuste automático especificado en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


Redimensiona la tabla y las celdas según el comportamiento de ajuste automático especificado.

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| comportamiento | Aspose::Words::Tables::AutoFitBehavior | Especifica cómo ajustar automáticamente la tabla. |
## Observaciones


Este método imita los comandos disponibles en el menú Auto Fit de una tabla en Microsoft Word. Los comandos disponibles son "Auto Fit to Contents", "Auto Fit to Window" y "Fixed Column Width". En Microsoft Word, estos comandos establecen las propiedades de tabla relevantes y luego actualizan el diseño de la tabla, y Aspose.Words hace lo mismo por usted.

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

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
