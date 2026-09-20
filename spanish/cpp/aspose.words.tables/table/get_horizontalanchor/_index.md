---
title: "Método Aspose::Words::Tables::Table::get_HorizontalAnchor"
linktitle: "get_HorizontalAnchor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::get_HorizontalAnchor. Obtiene el objeto base a partir del cual se debe calcular la posición horizontal de la tabla flotante. El valor predeterminado es Column en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


Obtiene el objeto base a partir del cual se debe calcular la posición horizontal de la tabla flotante. El valor predeterminado es [Column](../../../aspose.words.drawing/relativehorizontalposition/).

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
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

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
