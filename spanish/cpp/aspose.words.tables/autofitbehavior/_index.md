---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::AutoFitBehavior enum. Determina cómo Aspose.Words redimensiona la tabla cuando invoca el método AutoFit() en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Determina cómo Aspose.Words redimensiona la tabla cuando invoca el método [AutoFit()](../table/autofit/).

```cpp
enum class AutoFitBehavior
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words habilita la opción AutoFit, elimina el ancho preferido de la tabla y de todas las celdas y luego actualiza el diseño de la tabla. En la tabla resultante, los anchos de las celdas se actualizan para ajustarse al contenido de la tabla. Lo más probable es que la tabla se reduzca. |
| AutoFitToWindow | 1 | Cuando utiliza este valor, Aspose.Words habilita la opción AutoFit, establece el ancho preferido de la tabla al 100 %, elimina los anchos preferidos de todas las celdas y luego actualiza el diseño de la tabla. Como resultado, la tabla ocupa todo el ancho disponible y los anchos de las celdas se actualizan para ajustarse al contenido de la tabla. |
| FixedColumnWidths | 2 | Aspose.Words deshabilita la opción AutoFit y elimina el ancho preferido de la tabla. Los anchos de las celdas permanecen tal como se especifican en sus propiedades [Width](../cellformat/get_width/). |


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


Muestra cómo crear una tabla formateada de 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Al crear la tabla, el generador de documentos aplicará los valores actuales de las propiedades RowFormat/CellFormat.
// a la fila/celda actual donde está su cursor y a cualquier fila/celda nueva a medida que las crea.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Las filas y celdas añadidas previamente no se ven afectadas retroactivamente por cambios en el formato del generador.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Ver también

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
