---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale metodu"
linktitle: "get_BubbleScale"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale metodu. Baloncukların boyutunu varsayılan boyutlarının yüzde olarak alır veya ayarlar C++'da."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_bubblescale/
---
## ChartSeriesGroup::get_BubbleScale method


Baloncukların boyutunu varsayılan boyutlarının yüzdesi olarak alır veya ayarlar.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale()
```

## Açıklamalar


Yalnızca [Bubble](../../chartseriestype/) ve [Bubble3D](../../chartseriestype/) türlerinin seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 300 arasındadır, her iki uç dahil. Varsayılan değer 100'dür.

## Örnekler



Baloncukların boyutunu nasıl ayarlayacağınızı gösterin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir 3D baloncuk grafiği ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Baloncuk ölçeğini %200'e ayarlayın.
seriesGroup->set_BubbleScale(200);

doc->Save(get_ArtifactsDir() + u"Charts.BubbleScale.docx");
```

## Ayrıca Bakınız

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
