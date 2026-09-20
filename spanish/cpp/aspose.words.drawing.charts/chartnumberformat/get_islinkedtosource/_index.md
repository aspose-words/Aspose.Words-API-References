---
title: "Método Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource"
linktitle: "get_IsLinkedToSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource. Especifica si el código de formato está vinculado a una celda de origen. El valor predeterminado es true en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.drawing.charts/chartnumberformat/get_islinkedtosource/
---
## ChartNumberFormat::get_IsLinkedToSource method


Especifica si el código de formato está vinculado a una celda de origen. El valor predeterminado es verdadero.

```cpp
bool Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource()
```


## Ejemplos



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
