---
title: "Aspose::Words::Tables::CellFormat::get_Width método"
linktitle: "get_Width"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::CellFormat::get_Width método. Obtiene el ancho de la celda en puntos en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.tables/cellformat/get_width/
---
## CellFormat::get_Width method


Obtiene el ancho de la celda en puntos.

```cpp
double Aspose::Words::Tables::CellFormat::get_Width()
```

## Observaciones


El ancho se calcula por Aspose.Words al cargar y guardar el documento. Actualmente, no todas las combinaciones de tabla, celda y propiedades del documento son compatibles. El valor devuelto puede no ser preciso para algunos documentos. Puede no coincidir exactamente con el ancho de la celda calculado por MS Word cuando el documento se abre en MS Word.

No se recomienda establecer esta propiedad. No hay garantía de que la celda tenga realmente el ancho establecido. El ancho puede ajustarse para acomodar el contenido de la celda en un diseño de tabla de ajuste automático. Las celdas en otras filas pueden tener configuraciones de ancho conflictivas. La tabla puede redimensionarse para ajustarse al contenedor o cumplir con las configuraciones de ancho de tabla. Considere usar [PreferredWidth](../get_preferredwidth/) para establecer el ancho de la celda. Establecer esta propiedad define [PreferredWidth](../get_preferredwidth/) implícitamente desde la versión 15.8.

## Ejemplos



Muestra cómo crear una tabla con bordes personalizados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Configuración de opciones de formato de tabla para un DocumentBuilder
// se aplicarán a cada fila y celda que añadamos con él.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Cambiar el formato lo aplicará a la celda actual,
// y a cualquier celda nueva que creemos con el constructor posteriormente.
// Esto no afectará a las celdas que hemos añadido previamente.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Aumenta la altura de la fila para ajustar el texto vertical.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Muestra cómo formatear celdas con un constructor de documentos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Inserte una segunda celda y luego configure las opciones de relleno de texto de la celda.
// El constructor aplicará estas configuraciones en su celda actual, y cualquier celda nueva que se cree después.
builder->InsertCell();

System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = builder->get_CellFormat();
cellFormat->set_Width(250);
cellFormat->set_LeftPadding(30);
cellFormat->set_RightPadding(30);
cellFormat->set_TopPadding(30);
cellFormat->set_BottomPadding(30);

builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->EndTable();

// La primera celda no se vio afectada por la reconfiguración del relleno, y aún conserva los valores predeterminados.
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_BottomPadding());

ASPOSE_ASSERT_EQ(250.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_BottomPadding());

// La primera celda seguirá creciendo en el documento de salida para coincidir con el tamaño de su celda vecina.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## Ver también

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
