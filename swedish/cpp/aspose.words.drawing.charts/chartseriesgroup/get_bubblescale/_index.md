---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale metod"
linktitle: "get_BubbleScale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale metod. Hämtar eller anger storleken på bubblorna som en procentandel av deras standardstorlek i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Hämtar eller anger storleken på bubblorna som en procentandel av deras standardstorlek.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Anmärkningar


Gäller endast för seriegupper av typerna [Bubble](../../chartseriestype/) och [Bubble3D](../../chartseriestype/).

Det tillåtna värdeintervallet är från 0 till 300 inklusive. Standardvärdet är 100.

## Exempel



Visa hur man ställer in storleken på bubblorna.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett 3D-bubbel-diagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Ställ in bubbelskalan till 200 %.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## Se även

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
