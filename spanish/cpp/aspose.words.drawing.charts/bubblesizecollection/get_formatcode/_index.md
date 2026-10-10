---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode método"
linktitle: "get_FormatCode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode método. Obtiene o establece el código de formato aplicado a los tamaños de burbuja en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.drawing.charts/bubblesizecollection/get_formatcode/
---
## BubbleSizeCollection::get_FormatCode method


Obtiene o establece el código de formato aplicado a los tamaños de burbuja.

```cpp
System::String Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode()
```

## Observaciones


El formato de número se usa para cambiar la forma en que los valores aparecen en el gráfico. Los ejemplos de formatos numéricos:

Número - "#,##0.00"

Moneda - "\"\$\\"#,##0.00"

Hora - "[$-x-systime]h:mm:ss AM/PM"

Fecha - "d/mm/yyyy"

Porcentaje - "0.00%"

Fracción - "# ?/?"

Científico - "0.00E+00"

Contabilidad - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Personalizado con color - "[Red]-#,##0.0"

## Ejemplos



Muestra cómo trabajar con el código de formato de los datos del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un gráfico de burbujas.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Eliminar la serie generada por defecto.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Mostrar etiquetas de datos.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Establece códigos de formato de datos.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Ver también

* Class [BubbleSizeCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
