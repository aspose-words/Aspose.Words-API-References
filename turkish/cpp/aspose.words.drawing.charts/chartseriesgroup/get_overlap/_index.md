---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap metodu"
linktitle: "get_Overlap"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap metodu. Seri çubuklarının veya sütunlarının ne kadar örtüştüğünün yüzdesini C++'da alır veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Seri çubukları veya sütunlarının ne kadar üst üste geleceğinin yüzdesini alır veya ayarlar.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Açıklamalar


Tüm çubuk ve sütun türlerinin seri gruplarına uygulanır.

Kabul edilebilir değer aralığı -100 ile 100 arasındadır, her iki uç dahil. 0 değeri, çubuklar/sütunlar arasında boşluk olmadığını gösterir. Değer -100 ise, çubuklar/sütunlar arasındaki mesafe genişliklerine eşittir. 100 değeri, çubukların/sütunların tamamen üst üste geldiği anlamına gelir.

## Örnekler



Boşluk genişliği ve örtüşmeyi nasıl yapılandıracağınızı gösterin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Sütun boşluk genişliğini ve örtüşmeyi ayarlayın.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Ayrıca Bakınız

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
