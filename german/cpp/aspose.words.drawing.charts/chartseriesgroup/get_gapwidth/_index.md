---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth Methode"
linktitle: "get_GapWidth"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth Methode. Gibt den Prozentsatz der Lückenbreite zwischen Diagrammelementen zurück oder legt ihn fest in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Liest oder legt den Prozentsatz der Lückenbreite zwischen Diagrammelementen fest.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Hinweise


Gilt nur für Seriengruppen der Typen bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall und funnel.

Der zulässige Wertebereich liegt zwischen 0 und 500 einschließlich. Für bar-/column-basierte Seriengruppen stellt die Eigenschaft den Abstand zwischen Balkenclustern als Prozentsatz ihrer Breite dar. Für pie-of-pie- und bar-of-pie-Diagramme ist dies der Abstand zwischen den primären und sekundären Abschnitten des Diagramms.

## Beispiele



Zeigt, wie man die Lückenbreite und Überlappung konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Setzt die Spaltenlückenbreite und Überlappung.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Siehe auch

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
