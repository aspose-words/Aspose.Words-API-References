---
title: "تعداد Aspose::Words::Drawing::Charts::ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "عدد Aspose::Words::Drawing::Charts::ChartSeriesType. يحدد نوع سلسلة مخطط في C++."
type: docs
weight: 27500
url: /ar/cpp/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enum


يحدد نوع سلسلة المخطط.

```cpp
enum class ChartSeriesType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Area | 0 | يمثل سلسلة مخطط منطقة. |
| AreaStacked | 1 | يمثل سلسلة مخطط منطقة مكدسة. |
| AreaPercentStacked | 2 | يمثل سلسلة مخطط منطقة مكدسة بنسبة 100٪. |
| Area3D | 3 | يمثل سلسلة مخطط منطقة ثلاثية الأبعاد. |
| Area3DStacked | 4 | يمثل سلسلة مخطط منطقة مكدسة ثلاثية الأبعاد. |
| Area3DPercentStacked | 5 | يمثل سلسلة مخطط منطقة مكدسة بنسبة 100٪ ثلاثية الأبعاد. |
| Bar | 6 | يمثل سلسلة مخطط شريطي. |
| BarStacked | 7 | يمثل سلسلة مخطط شريطي مكدس. |
| BarPercentStacked | 8 | يمثل سلسلة مخطط شريطي مكدس بنسبة 100٪. |
| Bar3D | 9 | يمثل سلسلة مخطط شريطي ثلاثية الأبعاد. |
| Bar3DStacked | 10 | يمثل سلسلة مخطط شريطي مكدس ثلاثية الأبعاد. |
| Bar3DPercentStacked | 11 | يمثل سلسلة مخطط شريط ثلاثي الأبعاد مكدس 100٪. |
| Bubble | 12 | يمثل سلسلة مخطط فقاعة. |
| Bubble3D | 13 | يمثل سلسلة مخطط فقاعة ثلاثي الأبعاد. |
| عمود | 14 | يمثل سلسلة مخطط عمود. |
| ColumnStacked | 15 | يمثل سلسلة مخطط عمود مكدس. |
| ColumnPercentStacked | 16 | يمثل سلسلة مخطط عمود مكدس 100٪. |
| Column3D | 17 | يمثل سلسلة مخطط عمود ثلاثي الأبعاد. |
| Column3DStacked | 18 | يمثل سلسلة مخطط عمود مكدس ثلاثي الأبعاد. |
| Column3DPercentStacked | 19 | يمثل سلسلة مخطط عمود مكدس 100٪ ثلاثي الأبعاد. |
| Column3DClustered | 20 | يمثل سلسلة مخطط عمود متجمع ثلاثي الأبعاد. |
| دونات | 21 | يمثل سلسلة مخطط دونات. |
| خط | 22 | يمثل سلسلة مخطط خط. |
| LineStacked | 23 | يمثل سلسلة مخطط خط مكدس. |
| LinePercentStacked | 24 | يمثل سلسلة مخطط خط مكدس 100٪. |
| Line3D | 25 | يمثل سلسلة مخطط خط ثلاثي الأبعاد. |
| فطيرة | 26 | يمثل سلسلة مخطط دائري. |
| Pie3D | 27 | يمثل سلسلة مخطط دائري ثلاثي الأبعاد. |
| PieOfBar | 28 | يمثل سلسلة مخطط دائري من شريط. |
| PieOfPie | 29 | يمثل سلسلة مخطط دائري من دائري. |
| رادار | 30 | يمثل سلسلة مخطط رادار. |
| مبعثر | 31 | يمثل سلسلة مخطط مبعثر. |
| مخزون | 32 | يمثل سلسلة مخطط أسهم. |
| سطح | 33 | يمثل سلسلة مخطط سطح. |
| سطح ثلاثي الأبعاد | 34 | يمثل سلسلة مخطط سطح ثلاثي الأبعاد. |
| خريطة شجرية | 35 | يمثل سلسلة مخطط شجرة خريطة. |
| شعاع الشمس | 36 | يمثل سلسلة مخطط Sunburst. |
| هيستوجرام | 37 | يمثل سلسلة مخطط Histogram. |
| باريتو | 38 | يمثل سلسلة مخطط Pareto. |
| ParetoLine | 39 | يمثل سلسلة مخطط Pareto Line. |
| صندوق وشارب | 40 | يمثل سلسلة مخطط Box and Whisker. |
| شلال | 41 | يمثل سلسلة مخطط Waterfall. |
| قمع | 42 | يمثل سلسلة مخطط Funnel. |
| RegionMap | 43 | يمثل سلسلة مخطط Region Map. |


## أمثلة



يعرض كيفية إزالة سلسلة مخطط محددة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

// إزالة جميع السلاسل من نوع Column.
for (int32_t i = chart->get_Series()->get_Count() - 1; i >= 0; i--)
{
    if (chart->get_Series()->idx_get(i)->get_SeriesType() == Aspose::Words::Drawing::Charts::ChartSeriesType::Column)
    {
        chart->get_Series()->RemoveAt(i);
    }
}

chart->get_Series()->Add(u"Aspose Series", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"}), System::MakeArray<double>({5.6, 7.1, 2.9, 8.9}));

doc->Save(get_ArtifactsDir() + u"Charts.RemoveSpecificChartSeries.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
