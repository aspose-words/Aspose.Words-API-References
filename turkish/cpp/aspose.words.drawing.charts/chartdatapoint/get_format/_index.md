---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format metodu"
linktitle: "get_Format"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format metodu. Bu veri noktasının dolgu ve çizgi biçimlendirmesine C++'da erişim sağlar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.drawing.charts/chartdatapoint/get_format/
---
## ChartDataPoint::get_Format method


Bu veri noktasının dolgu ve çizgi biçimlendirmesine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartDataPoint::get_Format()
```


## Örnekler



Sütun grafiğinin kategorileri için bireysel biçimlendirme nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Varsayılan oluşturulan seriyi sil.
chart->get_Series()->Clear();

// Yeni seriler ekleniyor.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({1, 2, 3, 4}));

// Sütun biçimlendirmesini ayarla.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();
dataPoints->idx_get(0)->get_Format()->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Denim);
dataPoints->idx_get(1)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
dataPoints->idx_get(2)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
dataPoints->idx_get(3)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.DataPointsFormatting.docx");
```

## Ayrıca Bakınız

* Class [ChartFormat](../../chartformat/)
* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
