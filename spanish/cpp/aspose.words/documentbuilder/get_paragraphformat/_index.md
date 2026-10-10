---
title: "Aspose::Words::DocumentBuilder::get_ParagraphFormat método"
linktitle: "get_ParagraphFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::get_ParagraphFormat método. Devuelve un objeto que representa las propiedades de formato de párrafo actuales en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words/documentbuilder/get_paragraphformat/
---
## DocumentBuilder::get_ParagraphFormat method


Devuelve un objeto que representa las propiedades de formato de párrafo actuales.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::DocumentBuilder::get_ParagraphFormat()
```


## Ejemplos



Muestra cómo crear una tabla formateada usando [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// Establece algunas opciones de formato para el texto y la apariencia de la tabla.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// Configurar las opciones de formato en un document builder las aplicará
// a la celda/fila actual en la que está el cursor,
// así como a cualquier celda y fila nuevas creadas usando ese builder.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// Reconfigura los objetos de formato del builder para las nuevas filas y celdas que estamos a punto de crear.
// El builder no aplicará estos a la primera fila ya creada para que destaque como una fila de encabezado.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## Ver también

* Class [ParagraphFormat](../../paragraphformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
