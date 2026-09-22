---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntryCollection class"
linktitle: "ChartLegendEntryCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntryCollection class. Grafik lejand girişlerinin bir koleksiyonunu temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class


Grafik lejand girişlerinin bir koleksiyonunu temsil eder. Daha fazla bilgi için, [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) dokümantasyon makalesini ziyaret edin.

```cpp
class ChartLegendEntryCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Bu koleksiyondaki [ChartLegendEntry](../chartlegendentry/) sayısını döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeks için [ChartLegendEntry](../chartlegendentry/) döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



Bir grafik serisi için lejand girişinin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"});

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
series->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));
series->Add(u"Series 4", categories, System::MakeArray<double>({0, 0}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntryCollection> legendEntries = chart->get_Legend()->get_LegendEntries();
legendEntries->idx_get(3)->set_IsHidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.LegendEntries.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
