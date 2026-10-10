---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_XValues metodu"
linktitle: "get_XValues"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_XValues metodu. Bu grafik serisi için X değerlerinin bir koleksiyonunu C++'da alır."
type: docs
weight: 12334
url: /tr/cpp/aspose.words.drawing.charts/chartseries/get_xvalues/
---
## ChartSeries::get_XValues method


Bu grafik serisi için X değerlerinin bir koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValueCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_XValues()
```


## Örnekler



Grafik verisinin format kodu ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir Balon grafik ekle.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Varsayılan oluşturulan seriyi sil.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Veri etiketlerini göster.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Veri format kodlarını ayarla.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Ayrıca Bakınız

* Class [ChartXValueCollection](../../chartxvaluecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
