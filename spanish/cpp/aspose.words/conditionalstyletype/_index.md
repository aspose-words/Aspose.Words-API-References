---
title: "Aspose::Words::ConditionalStyleType enum"
linktitle: "ConditionalStyleType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ConditionalStyleType enum. Representa posibles áreas de tabla a las que se puede definir formato condicional en un estilo de tabla en C++."
type: docs
weight: 85000
url: /es/cpp/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enum


Representa las posibles áreas de tabla a las que se puede definir formato condicional en un estilo de tabla.

```cpp
enum class ConditionalStyleType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FirstRow | 0 | Especifica el formato de la primera fila de una tabla. |
| FirstColumn | 1 | Especifica el formato de la primera columna de una tabla. |
| LastRow | 2 | Especifica el formato de la última fila de una tabla. |
| LastColumn | 3 | Especifica el formato de la última columna de una tabla. |
| OddRowBanding | 4 | Especifica el formato de la franja de filas impares. |
| OddColumnBanding | 5 | Especifica el formato de la franja de columnas impares. |
| EvenRowBanding | 6 | Especifica el formato de la franja de filas pares. |
| EvenColumnBanding | 7 | Especifica el formato de la franja de columnas pares. |
| TopLeftCell | 8 | Especifica el formato de la celda superior izquierda de una tabla. |
| TopRightCell | 9 | Especifica el formato de la celda superior derecha de una tabla. |
| BottomLeftCell | 10 | Especifica el formato de la celda inferior izquierda de una tabla. |
| BottomRightCell | 11 | Especifica el formato de la celda inferior derecha de una tabla. |


## Ejemplos



Muestra cómo trabajar con ciertos estilos de área de una tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// Crea un estilo de tabla personalizado.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Los estilos condicionales son cambios de formato que afectan solo a algunas de las celdas de la tabla
// basado en un predicado, como que las celdas estén en la última fila.
// A continuación se presentan tres formas de acceder a los estilos condicionales de un estilo de tabla desde la colección "ConditionalStyles".
// 1 -  Por tipo de estilo:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  Por índice:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  Como una propiedad:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Aplica relleno y formato de texto a los estilos condicionales.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Enumera todas las condiciones de estilo posibles.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// Aplica el estilo personalizado, que contiene todos los estilos condicionales, a la tabla.
table->set_Style(tableStyle);

// Nuestro estilo aplica algunos estilos condicionales por defecto.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Necesitaremos habilitar todos los demás estilos nosotros mismos mediante la propiedad "StyleOptions".
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
