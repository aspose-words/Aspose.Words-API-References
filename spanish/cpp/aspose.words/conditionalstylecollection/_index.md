---
title: "Clase Aspose::Words::ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::ConditionalStyleCollection. Representa una colección de objetos ConditionalStyle. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Representa una colección de objetos [ConditionalStyle](../conditionalstyle/). Para obtener más información, visite el artículo de documentación [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Borra todos los estilos condicionales del estilo de tabla. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Obtiene el estilo de la celda inferior izquierda. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Obtiene el estilo de la celda inferior derecha. |
| [get_Count](./get_count/)() const | Obtiene el número de estilos condicionales en la colección. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Obtiene el estilo de bandas de columnas pares. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Obtiene el estilo de bandas de fila par. |
| [get_FirstColumn](./get_firstcolumn/)() | Obtiene el estilo de la primera columna. |
| [get_FirstRow](./get_firstrow/)() | Obtiene el estilo de la primera fila. |
| [get_LastColumn](./get_lastcolumn/)() | Obtiene el estilo de la última columna. |
| [get_LastRow](./get_lastrow/)() | Obtiene el estilo de la última fila. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Obtiene el estilo de bandas de columna impar. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Obtiene el estilo de bandas de fila impar. |
| [get_TopLeftCell](./get_topleftcell/)() | Obtiene el estilo de la celda superior izquierda. |
| [get_TopRightCell](./get_toprightcell/)() | Obtiene el estilo de la celda superior derecha. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los estilos condicionales en la colección. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Recupera un objeto [ConditionalStyle](../conditionalstyle/) por tipo de estilo condicional. |
| [idx_get](./idx_get/)(int32_t) | Recupera un objeto [ConditionalStyle](../conditionalstyle/) por índice. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
