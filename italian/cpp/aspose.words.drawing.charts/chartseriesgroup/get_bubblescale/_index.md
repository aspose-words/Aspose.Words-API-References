---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale metodo"
linktitle: "get_BubbleScale"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale metodo. Ottiene o imposta la dimensione delle bolle come percentuale della loro dimensione predefinita in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Ottiene o imposta la dimensione delle bolle come percentuale della loro dimensione predefinita.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Note


Si applica solo ai gruppi di serie dei tipi [Bubble](../../chartseriestype/) e [Bubble3D](../../chartseriestype/).

L'intervallo di valori accettabili è da 0 a 300 inclusi. Il valore predefinito è 100.

## Esempi



Mostra come impostare la dimensione delle bolle.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un grafico a bolle 3D.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Imposta la scala delle bolle al 200%.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## Vedi anche

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
