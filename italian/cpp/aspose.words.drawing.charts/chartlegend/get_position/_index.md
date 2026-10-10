---
title: "Metodo Aspose::Words::Drawing::Charts::ChartLegend::get_Position"
linktitle: "get_Position"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartLegend::get_Position. Specifica la posizione della legenda su un grafico in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing.charts/chartlegend/get_position/
---
## ChartLegend::get_Position method


Specifica la posizione della legenda su un grafico.

```cpp
Aspose::Words::Drawing::Charts::LegendPosition Aspose::Words::Drawing::Charts::ChartLegend::get_Position()
```


## Esempi



Mostra come modificare l'aspetto della legenda di un grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Sposta la legenda del grafico nell'angolo in alto a destra.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Concedi più spazio ad altri elementi del grafico, come il grafico stesso, permettendo loro di sovrapporsi alla legenda.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Vedi anche

* Enum [LegendPosition](../../legendposition/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
