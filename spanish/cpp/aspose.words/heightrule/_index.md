---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::HeightRule enum. Especifica la regla para determinar la altura de un objeto en C++."
type: docs
weight: 91000
url: /es/cpp/aspose.words/heightrule/
---
## HeightRule enum


Especifica la regla para determinar la altura de un objeto.

```cpp
enum class HeightRule
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AtLeast | 0 | La altura será al menos la altura especificada en puntos. Crecerá, si es necesario, para acomodar todo el texto dentro de un objeto. |
| Exactly | 1 | La altura se especifica exactamente en puntos. Tenga en cuenta que si el texto no cabe dentro del objeto con esta altura, aparecerá truncado. |
| Auto | 2 | La altura crecerá automáticamente para acomodar todo el texto dentro de un objeto. |


## Ejemplos



Muestra cómo formatear filas con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Inicie una segunda fila y luego configure su altura. El builder aplicará estos ajustes a
// su fila actual, así como a cualquier fila nueva que cree después.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// La primera fila no se vio afectada por la reconfiguración del relleno y aún mantiene los valores predeterminados.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
