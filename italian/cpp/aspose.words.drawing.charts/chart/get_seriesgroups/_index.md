---
title: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups metodo"
linktitle: "get_SeriesGroups"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups metodo. Fornisce l'accesso a una raccolta di gruppi di serie di questo grafico in C++."
type: docs
weight: 6500
url: /it/cpp/aspose.words.drawing.charts/chart/get_seriesgroups/
---
## Chart::get_SeriesGroups method


Fornisce l'accesso a una raccolta di gruppi di serie di questo grafico.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups()
```


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

* Class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
