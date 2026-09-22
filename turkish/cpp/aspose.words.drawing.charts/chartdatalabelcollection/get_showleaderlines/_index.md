---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines yöntemi"
linktitle: "get_ShowLeaderLines"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines yöntemi. Tüm serinin veri etiketleri için lider çizgilerin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer C++'da false'tur."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showleaderlines/
---
## ChartDataLabelCollection::get_ShowLeaderLines method


Tüm serinin veri etiketleri için veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye olanak tanır. Varsayılan değer **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines()
```

## Açıklamalar


Yalnızca pasta grafiklerde uygulanır. Lider çizgiler, bir veri etiketi ile ilgili veri noktası arasında görsel bir bağlantı oluşturur.

Bu özellik için tanımlanan değer, [ShowLeaderLines](../../chartdatalabel/get_showleaderlines/) özelliği kullanılarak bireysel bir veri etiketi için geçersiz kılınabilir.

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
