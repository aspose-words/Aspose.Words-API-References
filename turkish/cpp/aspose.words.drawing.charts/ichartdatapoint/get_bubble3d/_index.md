---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D metodu"
linktitle: "get_Bubble3D"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D metodu. C++'ta Balon grafiğindeki balonların 3B etkisi uygulanıp uygulanmayacağını belirtir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing.charts/ichartdatapoint/get_bubble3d/
---
## IChartDataPoint::get_Bubble3D method


Balon grafiğindeki balonların 3D etkisi uygulanıp uygulanmayacağını belirtir.

```cpp
virtual bool Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D()=0
```


## Örnekler



Balon grafiklerinde 3B efektlerin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Her balonun çapını gösteren bir veri etiketi uygula.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## Ayrıca Bakınız

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
