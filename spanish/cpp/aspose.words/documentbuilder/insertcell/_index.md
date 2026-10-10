---
title: "Aspose::Words::DocumentBuilder::InsertCell método"
linktitle: "InsertCell"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertCell método. Inserta una celda de tabla en el documento en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


Inserta una celda de tabla en el documento.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

El nodo de celda que acaba de insertarse.
## Observaciones


Para iniciar una tabla, simplemente llama a [InsertCell](./). Después de esto, cualquier contenido que agregues usando otros métodos de la clase [DocumentBuilder](../) se añadirá a la celda actual.

Para iniciar una nueva celda en la misma fila, llama a [InsertCell](./) de nuevo.

Para terminar una fila de tabla, llama a [EndRow](../endrow/).

Usa la propiedad [CellFormat](../get_cellformat/) para especificar el formato de la celda.

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


Muestra cómo usar un DocumentBuilder para crear una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inicia la tabla, luego rellena la primera fila con dos celdas.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Llama al método "EndRow" del constructor para iniciar una nueva fila.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Ver también

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
