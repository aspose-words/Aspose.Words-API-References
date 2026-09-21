---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth metod"
linktitle: "get_GapWidth"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth metod. Hämtar eller anger procentsatsen för gapbredden mellan diagramelement i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Hämtar eller anger procentandelen av mellanrumets bredd mellan diagramelement.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Anmärkningar


Gäller endast för seriegupper av typerna bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall och funnel.

Det tillåtna värdeintervallet är från 0 till 500 inklusive. För seriegupper baserade på bar/column representerar egenskapen avståndet mellan stapelkluster som en procentsats av deras bredd. För pie-of-pie och bar-of-pie diagram är detta avståndet mellan de primära och sekundära sektionerna i diagrammet.

## Exempel



Visa hur man konfigurerar gapbredd och överlappning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Ställ in kolumnens gapbredd och överlappning.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Se även

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
