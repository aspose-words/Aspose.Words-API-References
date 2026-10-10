---
title: "Aspose::Words::ConditionalStyle class"
linktitle: "ConditionalStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::ConditionalStyle. Representa un formato especial aplicado a alguna zona de una tabla con un estilo de tabla asignado. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


Representa un formato especial aplicado a una zona de una tabla con un estilo de tabla asignado. Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource,
                         public Aspose::Words::IShadingAttrSource,
                         public Aspose::Words::IParaAttrSource,
                         public Aspose::Words::IRunAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Borra el formato de este estilo condicional. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Compara este estilo condicional con el objeto especificado. |
| [get_Borders](./get_borders/)() | Obtiene la colección de bordes de celda predeterminados para el estilo condicional. |
| [get_BottomPadding](./get_bottompadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega debajo del contenido de las celdas de la tabla. |
| [get_Font](./get_font/)() | Obtiene el formato de caracteres del estilo condicional. |
| [get_LeftPadding](./get_leftpadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la izquierda del contenido de las celdas de la tabla. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Obtiene el formato de párrafo del estilo condicional. |
| [get_RightPadding](./get_rightpadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega a la derecha del contenido de las celdas de la tabla. |
| [get_Shading](./get_shading/)() | Obtiene un objeto [Shading](../shading/) que se refiere al formato de sombreado de este estilo condicional. |
| [get_TopPadding](./get_toppadding/)() | Obtiene o establece la cantidad de espacio (en puntos) que se agrega encima del contenido de las celdas de la tabla. |
| [get_Type](./get_type/)() | Obtiene el área de la tabla a la que se relaciona este estilo condicional. |
| [GetHashCode](./gethashcode/)() const override | Calcula el código hash para este objeto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Método set para [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Método set para [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/). |
| [set_RightPadding](./set_rightpadding/)(double) | Método set para [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Método set para [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/). |
| static [Type](./type/)() |  |

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
