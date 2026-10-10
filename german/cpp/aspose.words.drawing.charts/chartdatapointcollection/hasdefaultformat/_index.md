---
title: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat Methode"
linktitle: "HasDefaultFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat Methode. Gibt ein Flag zurück, das angibt, ob der Datenpunkt am angegebenen Index das Standardformat hat in C++."
type: docs
weight: 5500
url: /de/cpp/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection::HasDefaultFormat method


Ermittelt ein Flag, das angibt, ob der Datenpunkt am angegebenen Index das Standardformat hat.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat(int32_t dataPointIndex)
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

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
