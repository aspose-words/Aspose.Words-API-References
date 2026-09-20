---
title: "Enumeración Aspose::Words::Drawing::Charts::ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Drawing::Charts::ChartSeriesType. Especifica un tipo de serie de gráfico en C++."
type: docs
weight: 27500
url: /es/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


Especifica un tipo de serie de gráfico.

```cpp
enum class ChartSeriesType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Area | 0 | Representa una serie de gráfico de área. |
| AreaStacked | 1 | Representa una serie de gráfico de área apilada. |
| AreaPercentStacked | 2 | Representa una serie de gráfico de área apilada al 100%. |
| Area3D | 3 | Representa una serie de gráfico de área 3D. |
| Area3DStacked | 4 | Representa una serie de gráfico de área apilada 3D. |
| Area3DPercentStacked | 5 | Representa una serie de gráfico de área apilada al 100% 3D. |
| Bar | 6 | Representa una serie de gráfico de barras. |
| BarStacked | 7 | Representa una serie de gráfico de barras apiladas. |
| BarPercentStacked | 8 | Representa una serie de gráfico de barras apiladas al 100%. |
| Bar3D | 9 | Representa una serie de gráfico de barras 3D. |
| Bar3DStacked | 10 | Representa una serie de gráfico de barras apiladas 3D. |
| Bar3DPercentStacked | 11 | Representa una serie de gráfico de barras apiladas al 100% en 3D. |
| Bubble | 12 | Representa una serie de gráfico de burbujas. |
| Bubble3D | 13 | Representa una serie de gráfico de burbujas en 3D. |
| Columna | 14 | Representa una serie de gráfico de columnas. |
| ColumnStacked | 15 | Representa una serie de gráfico de columnas apiladas. |
| ColumnPercentStacked | 16 | Representa una serie de gráfico de columnas apiladas al 100%. |
| Column3D | 17 | Representa una serie de gráfico de columnas en 3D. |
| Column3DStacked | 18 | Representa una serie de gráfico de columnas apiladas en 3D. |
| Column3DPercentStacked | 19 | Representa una serie de gráfico de columnas apiladas al 100% en 3D. |
| Column3DClustered | 20 | Representa una serie de gráfico de columnas agrupadas en 3D. |
| Dona | 21 | Representa una serie de gráfico de rosquilla. |
| Línea | 22 | Representa una serie de gráfico de líneas. |
| LineStacked | 23 | Representa una serie de gráfico de líneas apiladas. |
| LinePercentStacked | 24 | Representa una serie de gráfico de líneas apiladas al 100%. |
| Line3D | 25 | Representa una serie de gráfico de líneas en 3D. |
| Tarta | 26 | Representa una serie de gráfico circular. |
| Pie3D | 27 | Representa una serie de gráfico circular en 3D. |
| PieOfBar | 28 | Representa una serie de gráfico de pastel de barras. |
| PieOfPie | 29 | Representa una serie de gráfico de pastel de pastel. |
| Radar | 30 | Representa una serie de gráfico de radar. |
| Dispersión | 31 | Representa una serie de gráfico de dispersión. |
| Acciones | 32 | Representa una serie de gráfico de acciones. |
| Superficie | 33 | Representa una serie de gráfico de superficie. |
| Surface3D | 34 | Representa una serie de gráfico de superficie en 3D. |
| Mapa de árbol | 35 | Representa una serie de gráfico de mapa de árbol. |
| Explosión | 36 | Representa una serie de gráfico Sunburst. |
| Histograma | 37 | Representa una serie de gráfico Histograma. |
| Pareto | 38 | Representa una serie de gráfico Pareto. |
| ParetoLine | 39 | Representa una serie de gráfico Pareto Line. |
| BoxAndWhisker | 40 | Representa una serie de gráfico Box and Whisker. |
| Cascada | 41 | Representa una serie de gráfico Waterfall. |
| Embudo | 42 | Representa una serie de gráfico Funnel. |
| RegionMap | 43 | Representa una serie de gráfico Region Map. |


## Ejemplos



Muestra cómo eliminar una serie de gráfico específica.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// Elimina todas las series del tipo Column.
for (int32_t i = chart->get_Series()->get_Count() - 1; i >= 0; i--)
{
    if (chart->get_Series()->idx_get(i)->get_SeriesType() == Aspose::Words::Drawing::Charts::ChartSeriesType::Column)
    {
        chart->get_Series()->RemoveAt(i);
    }
}

chart->get_Series()->Add(u"Aspose Series", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({5.6, 7.1, 2.9, 8.9}));

doc->Save(get_ArtifactsDir() + u"Charts.RemoveSpecificChartSeries.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
