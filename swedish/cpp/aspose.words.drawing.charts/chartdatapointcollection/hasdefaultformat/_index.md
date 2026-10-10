---
title: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat metod"
linktitle: "HasDefaultFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat metod. Hämtar en flagga som indikerar om datapunkten på det angivna indexet har standardformat i C++."
type: docs
weight: 5500
url: /sv/cpp/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection::HasDefaultFormat method


Hämtar en flagga som indikerar om datapunkten på det angivna indexet har standardformat.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataPointCollection::HasDefaultFormat(int32_t dataPointIndex)
```


## Exempel



Visar hur man kopierar datapunktformat.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Hämta diagrammet och serien för att uppdatera formatet.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// Kopiera formatet för datapunkten med index 1 till datapunkten med index 2
// så att datapunkt 2 ser likadan ut som datapunkt 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Kopiera formatet för datapunkten med index 0 till seriens standardinställningar så att alla datapunkter
// i serien som har standardformatet ser likadana ut som datapunkt 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## Se även

* Class [ChartDataPointCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
