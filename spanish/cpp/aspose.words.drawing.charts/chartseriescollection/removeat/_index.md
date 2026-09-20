---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection::RemoveAt method. Elimina una ChartSeries en el índice especificado en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing.charts/chartseriescollection/removeat/
---
## ChartSeriesCollection::RemoveAt method


Elimina una [ChartSeries](../../chartseries/) en el índice especificado.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesCollection::RemoveAt(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero de la [ChartSeries](../../chartseries/) a eliminar. |

## Ejemplos



Muestra cómo agregar y eliminar datos de series en un gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un gráfico de columnas que contendrá tres series de datos de demostración por defecto.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Cada serie tiene cuatro valores decimales: uno para cada una de las cuatro categorías.
// Cuatro grupos de tres columnas representarán estos datos.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Imprima el nombre de cada serie en el gráfico.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// Estos son los nombres de las categorías en el gráfico.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// Podemos añadir una serie con nuevos valores para las categorías existentes.
// Este gráfico ahora contendrá cuatro grupos de cuatro columnas.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// Una serie del gráfico también puede eliminarse por índice, así.
// Esto eliminará una de las tres series de demostración que venían con el gráfico.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// También podemos borrar todos los datos del gráfico de una vez con este método.
// Al crear un nuevo gráfico, esta es la forma de eliminar todos los datos de demostración
// antes de que podamos comenzar a trabajar en un gráfico en blanco.
chartData->Clear();
```

## Ver también

* Class [ChartSeriesCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
