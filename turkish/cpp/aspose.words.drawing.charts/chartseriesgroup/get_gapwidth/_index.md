---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth yöntemi"
linktitle: "get_GapWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth yöntemi. Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır veya ayarlar (C++)."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır veya ayarlar.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Açıklamalar


Yalnızca çubuk, sütun, çubuk-pasta, pasta-pasta, histogram, kutu&çubuk, şelale ve huni türlerinin seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 500 dahil arasındadır. Çubuk/sütun tabanlı seri grupları için, özellik çubuk kümeleri arasındaki boşluğu genişliklerinin yüzde olarak temsil eder. Pasta-pasta ve çubuk-pasta grafiklerinde ise bu, grafiğin birincil ve ikincil bölümleri arasındaki boşluktur.

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
