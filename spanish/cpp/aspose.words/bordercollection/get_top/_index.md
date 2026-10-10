---
title: "Método Aspose::Words::BorderCollection::get_Top"
linktitle: "get_Top"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BorderCollection::get_Top. Obtiene el borde superior en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/bordercollection/get_top/
---
## BorderCollection::get_Top method


Obtiene el borde superior.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Top()
```


## Ejemplos



Muestra cómo aplicar el color de borde y sombreado al crear una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inicia una tabla y establece un color/grosor predeterminado para sus bordes.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Crea una fila con dos celdas con diferentes colores de fondo.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Restablece el formato de la celda para desactivar los colores de fondo
// establece un grosor de borde personalizado para todas las celdas nuevas creadas por el generador,
// luego construye una segunda fila.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```

## Ver también

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
