---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap metod"
linktitle: "get_Overlap"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap metod. Hämtar eller anger procentandelen för hur mycket seriernas staplar eller kolumner överlappar i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Hämtar eller anger procentandelen av hur mycket seriernas staplar eller kolumner överlappar.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Anmärkningar


Gäller för seriegupper av alla stapel- och kolumntyper.

Det tillåtna värdeintervallet är från -100 till 100 inklusive. Ett värde på 0 indikerar att det inte finns något mellanrum mellan staplar/kolumner. Om värdet är -100 är avståndet mellan staplar/kolumner lika med deras bredd. Ett värde på 100 betyder att staplar/kolumner överlappar helt.

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
