---
title: "Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom method"
linktitle: "CopyFormatFrom"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom method. Kopiert das Standardformat des Datenpunkts vom Datenpunkt mit dem angegebenen Index in C++."
type: docs
weight: 1875
url: /de/cpp/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries::CopyFormatFrom method


Kopiert das Standardformat des Datenpunkts vom Datenpunkt mit dem angegebenen Index.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom(int32_t dataPointIndex)
```


## Beispiele



Zeigt, wie das Datenpunktformat kopiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Holen Sie das Diagramm und die Serie, um das Format zu aktualisieren.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Kopieren Sie das Format des Datenpunkts mit Index 1 zum Datenpunkt mit Index 2.
// so dass Datenpunkt 2 genauso aussieht wie Datenpunkt 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Kopieren Sie das Format des Datenpunkts mit Index 0 zu den Serien-Standardwerten, sodass alle Datenpunkte
// in der Serie, die das Standardformat haben, genauso aussehen wie Datenpunkt 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## Siehe auch

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
