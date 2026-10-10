---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize method"
linktitle: "get_SecondSectionSize"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize yöntemi. Yüzde olarak pasta grafiğinin ikincil bölümünün boyutunu alır veya ayarlar (C++)."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak alır veya ayarlar.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Açıklamalar


[PieOfPie](../../chartseriestype/) ve [PieOfBar](../../chartseriestype/) türlerinin seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 5 ile 200 arasındadır (her iki uç dahil). Varsayılan değer 75'tir.

## Örnekler



Pie of Pie grafiğinin nasıl oluşturulup biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Varsayılan oluşturulan seriyi sil.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Pie of Pie grafiğini biçimlendirin.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## Ayrıca Bakınız

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
