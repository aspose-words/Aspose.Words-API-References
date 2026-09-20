---
title: "Aspose::Words::Tables::Cell::get_LastParagraph método"
linktitle: "get_LastParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Cell::get_LastParagraph método. Obtiene el último párrafo entre los hijos inmediatos en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.tables/cell/get_lastparagraph/
---
## Cell::get_LastParagraph method


Obtiene el último párrafo entre los hijos inmediatos.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_LastParagraph()
```


## Ejemplos



Muestra cómo aplicar configuraciones a los bordes verticales al formato de una fila de tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea una tabla con bordes internos rojos y azules.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // Ajusta la apariencia de los bordes que aparecerán entre filas.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // Ajusta la apariencia de los bordes que aparecerán entre celdas.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// Un formato de fila y el párrafo interno de una celda usan configuraciones de borde diferentes.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## Ver también

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
