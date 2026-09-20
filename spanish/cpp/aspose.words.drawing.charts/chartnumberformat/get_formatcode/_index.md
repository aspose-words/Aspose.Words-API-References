---
title: "Método Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode"
linktitle: "get_FormatCode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode. Obtiene o establece el código de formato aplicado a una etiqueta de datos en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Obtiene o establece el código de formato aplicado a una etiqueta de datos.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Observaciones


El formato de número se utiliza para cambiar la forma en que un valor aparece en la etiqueta de datos y puede usarse de maneras muy creativas. Los ejemplos de formatos de número:

Número - "#,##0.00"

Moneda - "\"\$\\"#,##0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/yyyy"

Porcentaje - "0.00%"

Fracción - "# ?/?"

Científico - "0.00E+00"

Texto - "@"

Contabilidad - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Personalizado con color - "[Red]-#,##0.0"

## Ejemplos



Muestra cómo habilitar y configurar etiquetas de datos para una serie de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega un gráfico de líneas, luego elimina su serie de datos de demostración para comenzar con un gráfico limpio,
// y luego establece un título.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Inserta una serie de gráfico personalizada con los meses como categorías para el eje X,
// y los respectivos importes decimales para el eje Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Habilita las etiquetas de datos y luego aplica un formato numérico personalizado para los valores mostrados en las etiquetas de datos.
// Este formato tratará los valores decimales mostrados como millones de dólares estadounidenses.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```


Muestra cómo establecer el formato para los valores del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Agrega una serie personalizada al gráfico con categorías para el eje X,
// y valores numéricos grandes respectivos para el eje Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Establece el formato numérico de las etiquetas de marcas del eje Y para que no agrupe los dígitos con comas.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Esta bandera puede sobrescribir el valor anterior y obtener el formato numérico de la celda de origen.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## Ver también

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
