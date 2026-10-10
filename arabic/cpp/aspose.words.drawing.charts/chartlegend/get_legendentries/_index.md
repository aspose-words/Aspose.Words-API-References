---
title: "طريقة Aspose::Words::Drawing::Charts::ChartLegend::get_LegendEntries"
linktitle: "get_LegendEntries"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartLegend::get_LegendEntries. تُرجع مجموعة من مدخلات وسيلة الإيضاح لجميع السلاسل وخطوط الاتجاه للمخطط الأصلي في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing.charts/chartlegend/get_legendentries/
---
## ChartLegend::get_LegendEntries method


يرجع مجموعة من مدخلات وسيلة الإيضاح لجميع السلاسل وخطوط الاتجاه للمخطط الأصلي.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntryCollection> Aspose::Words::Drawing::Charts::ChartLegend::get_LegendEntries() const
```


## أمثلة



يعرض كيفية العمل مع إدخال وسيلة إيضاح لسلسلة المخطط.
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

## انظر أيضًا

* Class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
