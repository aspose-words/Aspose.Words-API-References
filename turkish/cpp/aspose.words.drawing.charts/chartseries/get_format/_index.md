---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format method"
linktitle: "get_Format"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format method. Serinin dolgu ve çizgi biçimlendirmesine C++'ta erişim sağlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing.charts/chartseries/get_format/
---
## ChartSeries::get_Format method


Serinin dolgu ve çizgi biçimlendirmesine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartSeries::get_Format()
```


## Örnekler



Seri rengini ayarlamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Varsayılan oluşturulan seriyi sil.
seriesColl->Clear();

// Kategori adları dizisi oluştur.
auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});

// Yeni seri ekleme. Değer ve kategori dizileri aynı boyutta olmalıdır.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = seriesColl->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = seriesColl->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = seriesColl->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));

// Seri rengini ayarla.
series1->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series2->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
series3->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.SeriesColor.docx");
```

## Ayrıca Bakınız

* Class [ChartFormat](../../chartformat/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
