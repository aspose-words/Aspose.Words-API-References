---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator yöntemi"
linktitle: "Aspose::Words::Fields::FieldMergeBarcode::get_ScalingFactor yöntemi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator yöntemi. Tüm serinin veri etiketleri için kullanılan dize ayırıcıyı alır veya ayarlar. Varsayılan olarak virgül kullanılır, yalnızca kategori adı ve yüzdeyi gösteren pasta grafiklerinde, C++'da bunun yerine satır sonu kullanılmalıdır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_separator/
---
## ChartDataLabelCollection::get_Separator method


Tüm serinin veri etiketleri için kullanılan dize ayırıcıyı alır veya ayarlar. Varsayılan olarak virgül kullanılır; yalnızca kategori adı ve yüzde gösteren pasta grafiklerinde bunun yerine satır sonu kullanılır.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator()
```


## Örnekler



Balon grafik veri etiketleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// Her balonun X/Y koordinatları ve çapı ile özel bir seri ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Veri etiketlerini etkinleştirin ve ardından görünümünü değiştirin.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```


Pasta grafik veri etiketleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// Temiz bir grafikle başlamak için grafiğin demo veri serisini temizleyin.
chart->get_Series()->Clear();

// Her dilim için bir kategori adı ve frekans tablosu içeren özel bir grafik serisi ekleyin.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// Her dilimin yüzde ve frekansını gösteren veri etiketlerini etkinleştirin ve görünümünü değiştirin.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## Ayrıca Bakınız

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
