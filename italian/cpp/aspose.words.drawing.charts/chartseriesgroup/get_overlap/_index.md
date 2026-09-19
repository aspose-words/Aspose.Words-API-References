---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap metodo"
linktitle: "get_Overlap"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap metodo. Ottiene o imposta la percentuale di sovrapposizione delle barre o colonne delle serie in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Ottiene o imposta la percentuale di quanto le barre o le colonne della serie si sovrappongono.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Note


Si applica ai gruppi di serie di tutti i tipi di barre e colonne.

L'intervallo di valori accettabili è da -100 a 100 inclusi. Un valore di 0 indica che non c'è spazio tra le barre/colonne. Se il valore è -100, la distanza tra le barre/colonne è pari alla loro larghezza. Un valore di 100 significa che le barre/colonne si sovrappongono completamente.

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
