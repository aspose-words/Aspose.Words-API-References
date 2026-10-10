---
title: "Aspose::Words::Tables::TableAlignment enum"
linktitle: "TableAlignment"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::TableAlignment enum. Especifica la alineación para una tabla en línea en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


Especifica la alineación para una tabla en línea.

```cpp
enum class TableAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Izquierda | 0 | La tabla está alineada a la izquierda. |
| Centro | 1 | La tabla está centrada. |
| Derecha | 2 | La tabla está alineada a la derecha. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
