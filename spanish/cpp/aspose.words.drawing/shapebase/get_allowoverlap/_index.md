---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap método"
linktitle: "get_AllowOverlap"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap método. Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Obtiene o establece un valor que especifica si esta forma puede superponerse a otras formas.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Observaciones


Esta propiedad afecta el comportamiento de la forma en Microsoft Word. Aspose.Words ignora el valor de esta propiedad.

Esta propiedad se aplica solo a formas de nivel superior.

El valor predeterminado es **true**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
