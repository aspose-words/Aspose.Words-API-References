---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth method"
linktitle: "get_GapWidth"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth method. Ottiene o imposta la percentuale di larghezza del gap tra gli elementi del grafico in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Ottiene o imposta la percentuale della larghezza dello spazio tra gli elementi del grafico.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Note


Si applica solo ai gruppi di serie dei tipi bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall e funnel.

L'intervallo di valori accettabili è da 0 a 500 inclusi. Per i gruppi di serie basati su bar/column, la proprietà rappresenta lo spazio tra i raggruppamenti di barre come percentuale della loro larghezza. Per i grafici pie-of-pie e bar-of-pie, questo è lo spazio tra le sezioni primaria e secondaria del grafico.

## Esempi



Mostra come configurare la larghezza del gap e la sovrapposizione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Imposta la larghezza del gap della colonna e la sovrapposizione.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Vedi anche

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
