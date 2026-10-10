---
title: "Aspose::Words::Drawing::Charts::ChartYValueCollection clase"
linktitle: "ChartYValueCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartYValueCollection clase. Representa una colección de valores Y para una serie de gráfico en C++."
type: docs
weight: 18800
url: /es/cpp/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class


Representa una colección de valores Y para una serie de gráfico.

```cpp
class ChartYValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Count](./get_count/)() | Obtiene el número de elementos en esta colección. |
| [get_FormatCode](./get_formatcode/)() | Obtiene o establece el código de formato aplicado a los valores Y. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece el valor Y en el índice especificado. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Obtiene o establece el valor Y en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Método setter para [Aspose::Words::Drawing::Charts::ChartYValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Observaciones


Todos los elementos de la colección, excepto **null**, deben tener el mismo [ValueType](../chartyvalue/get_valuetype/).

La colección solo permite cambiar valores Y. Para agregar o insertar nuevos valores a una serie de gráfico, o eliminar valores, se pueden usar los métodos apropiados de la clase [ChartSeries](../chartseries/).

## Ejemplos



Muestra cómo obtener los datos de la serie del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // Borre el formato individual de todos los puntos de datos.
    // Los puntos de datos y los valores de datos son uno a uno en los gráficos de columnas.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // Obtener el valor Y.
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Cambiar los colores de los valores máximo y mínimo.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
