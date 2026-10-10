---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize yöntemi"
linktitle: "get_DoughnutHoleSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize yöntemi. Ebeveyn halka grafiğinin delik boyutunu yüzde olarak alır veya ayarlar (C++)."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_doughnutholesize/
---
## ChartSeriesGroup::get_DoughnutHoleSize method


Üst dönen çember grafiğinin delik boyutunu yüzde olarak alır veya ayarlar.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize()
```

## Açıklamalar


[Doughnut](../../chartseriestype/) türünün seri gruplarına yalnızca uygulanır.

Kabul edilebilir değer aralığı 0 ile 90 arasındadır (her iki uç dahil). Varsayılan değer 75'tir.

## Örnekler



Doughnut grafiğini oluşturma ve biçimlendirme nasıl yapılır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Varsayılan oluşturulan seriyi sil.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Doughnut grafiğini biçimlendir.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## Ayrıca Bakınız

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
