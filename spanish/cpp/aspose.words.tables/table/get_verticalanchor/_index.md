---
title: "Método Aspose::Words::Tables::Table::get_VerticalAnchor"
linktitle: "get_VerticalAnchor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::get_VerticalAnchor. Obtiene el objeto base a partir del cual se debe calcular la posición vertical de la tabla flotante. El valor predeterminado es Margin en C++."
type: docs
weight: 41000
url: /es/cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Obtiene el objeto base a partir del cual se debe calcular la posición vertical de la tabla flotante. El valor predeterminado es [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
```


## Ejemplos



Muestra cómo trabajar con las propiedades de tablas flotantes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Solo Margin, Page, Column están disponibles en RelativeHorizontalPosition para el setter HorizontalAnchor.
    // Se lanzará ArgumentException para cualquier otro valor.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Solo Margin, Page, Paragraph están disponibles en RelativeVerticalPosition para el setter VerticalAnchor.
    // Se lanzará ArgumentException para cualquier otro valor.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Ver también

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
