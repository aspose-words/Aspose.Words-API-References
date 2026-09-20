---
title: "Método Aspose::Words::Tables::Table::ClearBorders"
linktitle: "ClearBorders"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::ClearBorders. Elimina todos los bordes de tabla y celda en esta tabla en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.tables/table/clearborders/
---
## Table::ClearBorders method


Elimina todos los bordes de tabla y celda en esta tabla.

```cpp
void Aspose::Words::Tables::Table::ClearBorders()
```


## Ejemplos



Muestra cómo aplicar un borde de contorno a una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Alinea la tabla al centro de la página.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Elimina cualquier borde y sombreado existente de la tabla.
table->ClearBorders();
table->ClearShading();

// Añade bordes verdes al contorno de la tabla.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Rellena las celdas con un color sólido verde claro.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```


Muestra cómo eliminar todos los bordes de una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

// Modifica el color y el grosor del borde superior.
System::SharedPtr<Aspose::Words::Border> topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Double, 1.5, System::Drawing::Color::get_Red(), true);

ASPOSE_ASSERT_EQ(1.5, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Double, topBorder->get_LineStyle());

// Elimina los bordes de todas las celdas de la tabla y luego guarda el documento.
table->ClearBorders();
doc->Save(get_ArtifactsDir() + u"Table.ClearBorders.docx");

// Verifica los valores de las propiedades de la tabla después de volver a abrir el documento.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.ClearBorders.docx");
table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);

ASPOSE_ASSERT_EQ(0.0, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::None, topBorder->get_LineStyle());
```

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
