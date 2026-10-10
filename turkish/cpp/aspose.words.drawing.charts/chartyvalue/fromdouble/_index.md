---
title: "Aspose::Words::Drawing::Charts::ChartYValue::FromDouble yöntemi"
linktitle: "FromDouble"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartYValue::FromDouble yöntemi. C++'ta Double türünde bir ChartYValue örneği oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing.charts/chartyvalue/fromdouble/
---
## ChartYValue::FromDouble method


[ChartYValue](../) tipinde bir [Double](../../chartyvaluetype/) örneği oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(double value)
```


## Örnekler



Grafik serilerini veriyle doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// İlk serinin X ve Y değerlerini temizle.
series1->ClearValues();

// Seriyi veriyle doldur.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// İkinci serinin X ve Y değerlerini temizle.
series2->Clear();

// Seriyi veriyle doldur.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Ayrıca Bakınız

* Class [ChartYValue](../)
* Class [ChartYValue](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
