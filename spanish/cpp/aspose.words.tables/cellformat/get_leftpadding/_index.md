---
title: "Aspose::Words::Tables::CellFormat::get_LeftPadding método"
linktitle: "get_LeftPadding"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::CellFormat::get_LeftPadding método. Devuelve o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de la celda en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.tables/cellformat/get_leftpadding/
---
## CellFormat::get_LeftPadding method


Devuelve o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de la celda.

```cpp
double Aspose::Words::Tables::CellFormat::get_LeftPadding()
```


## Ejemplos



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
