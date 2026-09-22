---
title: "Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom method"
linktitle: "CopyFormatFrom"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom method. Belirtilen indeksteki veri noktasından varsayılan veri noktası biçimini C++'ta kopyalar."
type: docs
weight: 1875
url: /tr/cpp/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries::CopyFormatFrom method


Belirtilen dizine sahip veri noktasından varsayılan veri noktası biçimini kopyalar.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom(int32_t dataPointIndex)
```


## Örnekler



Veri noktası biçimini kopyalamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// Biçimi güncellemek için grafiği ve seriyi alın.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// İndeks 1'deki veri noktasının biçimini indeks 2'deki veri noktasına kopyala
// böylece veri noktası 2, veri noktası 1 gibi görünür.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// Veri noktasının 0 indeksindeki biçimini serinin varsayılanlarına kopyalayın, böylece tüm veri noktaları
// Varsayılan biçime sahip serideki veri noktaları, veri noktası 0 ile aynı görünsün.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## Ayrıca Bakınız

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
