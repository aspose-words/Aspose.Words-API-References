---
title: "Aspose::Words::ConditionalStyleCollection::ClearFormatting método"
linktitle: "ClearFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting método. Elimina todos los estilos condicionales del estilo de tabla en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


Borra todos los estilos condicionales del estilo de tabla.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## Ejemplos



Muestra cómo restablecer los estilos de tabla condicionales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// Establece el estilo de tabla para colorear los bordes de la primera fila de la tabla en rojo.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Establece el estilo de tabla para colorear los bordes de la última fila de la tabla en azul.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// A continuación se presentan dos formas de usar el método "ClearFormatting" para borrar los estilos condicionales.
// 1 -  Borrar los estilos condicionales para una parte específica de una tabla:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Borrar los estilos condicionales para toda la tabla:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## Ver también

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
