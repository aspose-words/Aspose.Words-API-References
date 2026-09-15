---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection class"
linktitle: "ChartSeriesGroupCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection class. تمثّل مجموعة من كائنات ChartSeriesGroup في C++."
type: docs
weight: 17667
url: /ar/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class


تمثّل مجموعة من كائنات [ChartSeriesGroup](../chartseriesgroup/).

```cpp
class ChartSeriesGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(Aspose::Words::Drawing::Charts::ChartSeriesType) | يضيف مجموعة سلسلة جديدة من النوع المحدد إلى هذه المجموعة. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يرجع عدد مجموعات السلاسل في هذه المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يرجع [ChartSeriesGroup](../chartseriesgroup/) في الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | يزيل مجموعة سلسلة في الفهرس المحدد. سيتم إزالة جميع السلاسل الفرعية من الرسم البياني. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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
