---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. C++'da bir grafik veri etiketinin konumunu belirtir."
type: docs
weight: 27334
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Bir grafik veri etiketi için konumu belirtir.

```cpp
enum class ChartDataLabelPosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Orta | 0 | Bir veri etiketinin veri işaretleyicisinin ortasında görüntülenmesi gerektiğini belirtir. |
| Sol | 1 | Bir veri etiketinin veri işaretleyicisinin solunda görüntülenmesi gerektiğini belirtir. |
| Sağ | 2 | Bir veri etiketinin veri işaretleyicisinin sağında görüntülenmesi gerektiğini belirtir. |
| Üstünde | 3 | Bir veri etiketinin veri işaretleyicisinin üzerinde görüntülenmesi gerektiğini belirtir. |
| Aşağıda | 4 | Bir veri etiketinin veri işaretleyicisinin altında görüntülenmesi gerektiğini belirtir. |
| InsideBase | 5 | Bir veri etiketinin veri işaretleyicisinin tabanının içinde görüntülenmesi gerektiğini belirtir. |
| InsideEnd | 6 | Bir veri etiketinin veri işaretleyicisinin ucunun içinde görüntülenmesi gerektiğini belirtir. |
| OutsideEnd | 7 | Bir veri etiketinin veri işaretçisinin ucunun dışında görüntülenmesi gerektiğini belirtir. |
| BestFit | 8 | Bir veri etiketinin en uygun konumda görüntülenmesi gerektiğini belirtir. |


## Örnekler



Veri etiketinin konumunun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Sütun grafiği ekle.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Varsayılan oluşturulan seriyi sil.
seriesColl->Clear();

// Seri ekle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Veri etiketlerini göster ve yazı tipi rengini ayarla.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Veri etiketi konumunu ayarla.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
