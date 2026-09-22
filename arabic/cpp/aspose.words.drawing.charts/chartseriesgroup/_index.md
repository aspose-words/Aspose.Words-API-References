---
title: "فئة Aspose::Words::Drawing::Charts::ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Drawing::Charts::ChartSeriesGroup. تمثل خصائص مجموعة سلسلة المخطط، أي خصائص سلاسل المخطط من نفس النوع المرتبطة بنفس المحاور في C++."
type: docs
weight: 17334
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class


يمثل خصائص مجموعة سلاسل المخطط، أي خصائص سلاسل المخطط من نفس النوع المرتبطة بنفس المحاور.

```cpp
class ChartSeriesGroup : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AxisGroup](./get_axisgroup/)() | يحصل أو يعيّن مجموعة المحاور التي تنتمي إليها مجموعة السلاسل هذه. |
| [get_AxisX](./get_axisx/)() | يوفر الوصول إلى خصائص المحور X لمجموعة السلاسل هذه. |
| [get_AxisY](./get_axisy/)() | يوفر الوصول إلى خصائص المحور Y لمجموعة السلاسل هذه. |
| [get_BubbleScale](./get_bubblescale/)() | يحصل أو يعيّن حجم الفقاعات كنسبة مئوية من حجمها الافتراضي. |
| [get_DoughnutHoleSize](./get_doughnutholesize/)() | يحصل أو يعيّن حجم الفتحة في مخطط الدونات الأب كنسبة مئوية. |
| [get_FirstSliceAngle](./get_firstsliceangle/)() | يحصل أو يعيّن الزاوية، بالدرجات، للقطعة الأولى في مخطط الفطيرة الأب. |
| [get_GapWidth](./get_gapwidth/)() | يحصل أو يعيّن نسبة عرض الفجوة بين عناصر المخطط. |
| [get_Overlap](./get_overlap/)() | يحصل أو يضبط النسبة المئوية لمقدار تداخل أشرطة أو أعمدة السلسلة. |
| [get_SecondSectionSize](./get_secondsectionsize/)() | يحصل أو يضبط حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية. |
| [get_Series](./get_series/)() | يحصل على مجموعة من السلاسل التي تنتمي إلى مجموعة السلاسل هذه. |
| [get_SeriesType](./get_seriestype/)() | يحصل على نوع سلاسل المخطط المتضمنة في هذه المجموعة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AxisGroup](./set_axisgroup/)(Aspose::Words::Drawing::Charts::AxisGroup) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_AxisGroup](./get_axisgroup/). |
| [set_BubbleScale](./set_bubblescale/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_BubbleScale](./get_bubblescale/). |
| [set_DoughnutHoleSize](./set_doughnutholesize/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize](./get_doughnutholesize/). |
| [set_FirstSliceAngle](./set_firstsliceangle/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle](./get_firstsliceangle/). |
| [set_GapWidth](./set_gapwidth/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth](./get_gapwidth/). |
| [set_Overlap](./set_overlap/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap](./get_overlap/). |
| [set_SecondSectionSize](./set_secondsectionsize/)(int32_t) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize](./get_secondsectionsize/). |
| static [Type](./type/)() |  |
## ملاحظات


تحتوي المخططات المركبة على مجموعات متعددة من سلاسل المخططات، مع مجموعة منفصلة لكل نوع من السلاسل.

كما يمكنك إنشاء مجموعة سلاسل مخطط لتعيين محاور ثانوية لسلسلة أو أكثر من سلاسل المخطط.

لمزيد من المعلومات، زر مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

## أمثلة



يوضح كيفية العمل مع المحور الثانوي للرسم البياني.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// حذف السلسلة التي تم إنشاؤها افتراضيًا.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// أنشئ مجموعة سلسلة إضافية، أيضًا من نوع الخط.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// حدد استخدام المحاور الثانوية لمجموعة السلسلة الجديدة.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// إخفاء المحور X الثانوي.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// حدد عنوان المحور Y الثانوي.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// أضف سلسلة إلى مجموعة السلسلة الجديدة.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
