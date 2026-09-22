---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Remove metodu"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Remove metodu. Belirtilen indeksdeki grafik serisinden X değeri, Y değeri ve destekleniyorsa balon boyutunu kaldırır. İlgili veri noktası ve veri etiketi de C++'ta kaldırılır."
type: docs
weight: 14500
url: /tr/cpp/aspose.words.drawing.charts/chartseries/remove/
---
## ChartSeries::Remove method


Destekleniyorsa, belirtilen indekste grafik serisinden X değeri, Y değeri ve baloncuk boyutunu kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Remove(int32_t index)
```


## Örnekler



Grafik veri değerlerini ekleme/kaldırmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Her iki serideki ilk değeri kaldır.
department1Series->Remove(0);
department2Series->Remove(0);

// Her iki seriye yeni değerler ekle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Ayrıca Bakınız

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
