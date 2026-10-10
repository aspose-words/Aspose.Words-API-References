---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage metodu"
linktitle: "get_ShowPercentage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage metodu. Yüzde değerinin tüm serinin veri etiketlerinde gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer false'tur. Yalnızca C++'daki Pie grafiklerinde uygulanır."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showpercentage/
---
## ChartDataLabelCollection::get_ShowPercentage method


Tüm serinin veri etiketlerinde yüzde değerinin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**. Yalnızca Pasta grafiklerinde uygulanır.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage()
```


## Örnekler



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
