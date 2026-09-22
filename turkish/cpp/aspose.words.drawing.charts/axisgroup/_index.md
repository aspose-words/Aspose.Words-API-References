---
title: "Aspose::Words::Drawing::Charts::AxisGroup enum"
linktitle: "AxisGroup"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::AxisGroup enum. C++'da bir grafik eksen grubunun türünü temsil eder."
type: docs
weight: 22500
url: /tr/cpp/aspose.words.drawing.charts/axisgroup/
---
## AxisGroup enum


Bir grafik eksen grubu tipini temsil eder.

```cpp
enum class AxisGroup
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Birincil | 0 | Birincil eksen grubunu belirtir. |
| İkincil | 1 | İkincil eksen grubunu belirtir. |


## Örnekler



Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Varsayılan oluşturulan seriyi sil.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Ayrıca çizgi tipi bir ek seri grubu oluşturun.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Yeni seri grubu için ikincil eksenlerin kullanımını belirtin.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// İkincil X eksenini gizle.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// İkincil Y ekseninin başlığını tanımla.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Yeni seri grubuna bir seri ekle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
