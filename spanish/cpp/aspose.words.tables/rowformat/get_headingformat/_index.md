---
title: "Método Aspose::Words::Tables::RowFormat::get_HeadingFormat"
linktitle: "get_HeadingFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::RowFormat::get_HeadingFormat. Verdadero si la fila se repite como encabezado de tabla en cada página cuando la tabla abarca más de una página en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


Verdadero si la fila se repite como encabezado de tabla en cada página cuando la tabla abarca más de una página.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Ejemplos



Muestra cómo crear una tabla con filas que se repiten en cada página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Cualquier fila insertada mientras la bandera "HeadingFormat" está establecida en "true"
// aparecerá en la parte superior de la tabla en cada página que abarque.
builder->get_RowFormat()->set_HeadingFormat(true);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_CellFormat()->set_Width(100);
builder->InsertCell();
builder->Write(u"Heading row 1");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Heading row 2");
builder->EndRow();

builder->get_CellFormat()->set_Width(50);
builder->get_ParagraphFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeadingFormat(false);

// Agregue suficientes filas para que la tabla abarque dos páginas.
for (int32_t i = 0; i < 50; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 1.", table->get_Rows()->get_Count()));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 2.", table->get_Rows()->get_Count()));
    builder->EndRow();
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableSetHeadingRow.docx");
```

## Ver también

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
