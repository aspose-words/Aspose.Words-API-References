---
title: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat metod"
linktitle: "CopyFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat metod. Kopierar format från källdatapunkten till destinationsdatapunkten i C++."
type: docs
weight: 2500
url: /sv/cpp/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection::CopyFormat method


Kopierar format från källdatapunkten till destinationsdatapunkten.

```cpp
void Aspose::Words::Drawing::Charts::ChartDataPointCollection::CopyFormat(int32_t sourceIndex, int32_t destinationIndex)
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
