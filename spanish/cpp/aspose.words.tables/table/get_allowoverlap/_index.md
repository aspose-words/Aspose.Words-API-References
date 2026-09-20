---
title: "Método Aspose::Words::Tables::Table::get_AllowOverlap"
linktitle: "get_AllowOverlap"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Tables::Table::get_AllowOverlap. Obtiene si una tabla flotante debe permitir que otros objetos flotantes en el documento se superpongan a sus límites cuando se muestra. El valor predeterminado es true en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Obtiene si una tabla flotante debe permitir que otros objetos flotantes en el documento se superpongan a sus límites cuando se muestra. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
