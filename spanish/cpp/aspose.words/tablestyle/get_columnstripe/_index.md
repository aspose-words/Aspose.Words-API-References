---
title: "Aspose::Words::TableStyle::get_ColumnStripe method"
linktitle: "get_ColumnStripe"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TableStyle::get_ColumnStripe method. Obtiene o establece un número de columnas para incluir en el agrupamiento cuando el estilo especifica agrupamiento de columnas impares/pares en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Obtiene o establece un número de columnas para incluir en el bandado cuando el estilo especifica bandado de columnas impares/pares.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Ejemplos



Muestra cómo crear estilos de tabla condicionales que alternan entre filas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Podemos configurar un estilo condicional de una tabla para aplicar un color diferente a la fila/columna,
// basado en si la fila/columna es par o impar, creando un patrón de colores alternado.
// También podemos aplicar un número n al agrupamiento de filas/columnas,
// lo que significa que el color alterna después de cada n filas/columnas en lugar de una.
// Cree una tabla donde columnas y filas individuales se agrupen en tríos.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// Aplique un estilo de línea a todos los bordes de la tabla.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Establezca los dos colores, que alternarán cada 3 filas.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Establezca un color para aplicar a cada columna par, que sobrescribirá cualquier coloración personalizada de filas.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// La propiedad "StyleOptions" habilita el agrupamiento de filas por defecto.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Utilice también la propiedad "StyleOptions" para habilitar el agrupamiento de columnas.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## Ver también

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
