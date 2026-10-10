---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextOrientation enum. Especifica la orientación del texto en una página, en una celda de tabla o en un marco de texto en C++."
type: docs
weight: 124000
url: /es/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Especifica la orientación del texto en una página, en una celda de tabla o en un marco de texto.

```cpp
enum class TextOrientation
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | 0 | El texto se dispone horizontalmente (lr-tb). |
| Hacia abajo | 1 | El texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl). |
| Hacia arriba | 3 | El texto se rota 90 grados a la izquierda para aparecer de abajo a arriba (bt-lr). |
| HorizontalRotatedFarEast | 4 | El texto se dispone horizontalmente, pero los caracteres de Asia Oriental se rotan 90 grados a la izquierda (lr-tb-v). |
| VerticalFarEast | 5 | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo (tb-rl-v). |
| VerticalRotatedFarEast | 7 | Los caracteres del Lejano Oriente aparecen verticales, el resto del texto se rota 90 grados a la derecha para aparecer de arriba a abajo verticalmente, luego de izquierda a derecha horizontalmente (tb-lr-v). |


## Ejemplos



Muestra cómo crear una tabla formateada de 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Al crear la tabla, el generador de documentos aplicará los valores actuales de las propiedades RowFormat/CellFormat.
// a la fila/celda actual donde está su cursor y a cualquier fila/celda nueva a medida que las crea.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Las filas y celdas añadidas previamente no se ven afectadas retroactivamente por cambios en el formato del generador.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
