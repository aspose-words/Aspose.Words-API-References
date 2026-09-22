---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels yöntemi"
linktitle: "get_HasDataLabels"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels yöntemi. Seriler için veri etiketlerinin gösterilip gösterilmeyeceğini belirten bir bayrağı alır veya ayarlar (C++)."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.drawing.charts/chartseries/get_hasdatalabels/
---
## ChartSeries::get_HasDataLabels method


Seri için veri etiketlerinin görüntülenip görüntülenmeyeceğini gösteren bir bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels() const
```


## Örnekler



Bir grafik serisi için veri etiketlerini nasıl etkinleştirip yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir çizgi grafik ekleyin, ardından temiz bir grafikle başlamak için demo veri serisini temizleyin,
// ve ardından bir başlık ayarlayın.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// X ekseni için ayları kategori olarak kullanan özel bir grafik serisi ekleyin,
// ve Y ekseni için ilgili ondalık miktarları belirtin.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Veri etiketlerini etkinleştirin ve ardından veri etiketlerinde gösterilen değerler için özel bir sayı biçimi uygulayın.
// Bu biçim, gösterilen ondalık değerleri ABD Doları milyonları olarak ele alacaktır.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## Ayrıca Bakınız

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
