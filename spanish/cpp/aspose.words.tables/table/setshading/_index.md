---
title: "Método Aspose::Words::Tables::Table::SetShading"
linktitle: "SetShading"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::SetShading. Establece el sombreado a los valores especificados en toda la tabla en C++."
type: docs
weight: 70000
url: /es/cpp/aspose.words.tables/table/setshading/
---
## Table::SetShading method


Establece el sombreado a los valores especificados en toda la tabla.

```cpp
void Aspose::Words::Tables::Table::SetShading(Aspose::Words::TextureIndex texture, System::Drawing::Color foregroundColor, System::Drawing::Color backgroundColor)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textura | Aspose::Words::TextureIndex | La textura a aplicar. |
| foregroundColor | System::Drawing::Color | El color de la textura. |
| backgroundColor | System::Drawing::Color | El color del relleno de fondo. |

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

## Ver también

* Enum [TextureIndex](../../../aspose.words/textureindex/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
