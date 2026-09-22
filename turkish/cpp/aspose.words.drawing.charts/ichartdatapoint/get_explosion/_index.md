---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion metodu"
linktitle: "get_Explosion"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion metodu. Veri noktasının pasta grafiğinin merkezinden ne kadar uzaklaştırılacağını belirtir. Negatif olabilir, negatif olması özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca C++'ta Pasta grafiklerinde geçerlidir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing.charts/ichartdatapoint/get_explosion/
---
## IChartDataPoint::get_Explosion method


Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. Negatif olabilir; negatif, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir.

```cpp
virtual int32_t Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion()=0
```


## Örnekler



Bir pasta grafiğinin dilimlerini merkezden uzaklaştırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" bir pasta grafiğinin dilimlerini, ilgili veri noktasının Explosion özelliği aracılığıyla bir mesafe kadar merkezden uzaklaştırabilir.
// Pasta grafiğinin ilk bölümüne bir veri noktası ekleyin ve onu merkezden 10 puan uzaklaştırın.
// Aspose.Words, mevcut değilse veri noktalarını otomatik olarak oluşturur.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// İkinci bölümü daha büyük bir mesafe ile kaydırın.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## Ayrıca Bakınız

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
