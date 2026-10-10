---
title: "Aspose::Words::Drawing::Charts::ChartSeriesCollection class"
linktitle: "ChartSeriesCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesCollection class. يمثل مجموعة من ChartSeries. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


يمثل مجموعة من [ChartSeries](../chartseries/). لمعرفة المزيد، زر مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | يضيف [ChartSeries](../chartseries/) جديدًا إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلاسل إلى أي نوع من مخططات Bar و Column و Line و Surface. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | يضيف [ChartSeries](../chartseries/) جديدًا إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلاسل إلى أي نوع من مخططات Scatter. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | يضيف [ChartSeries](../chartseries/) جديدًا إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلاسل إلى أي نوع من مخططات Area و Radar و Stock. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | يضيف [ChartSeries](../chartseries/) جديدًا إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلاسل إلى أي نوع من مخططات Bubble. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | يضيف [ChartSeries](../chartseries/) جديدًا إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلاسل تحتوي على فئات بيانات متعددة المستويات. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | يضيف [ChartSeries](../chartseries/) جديدًا إلى هذه المجموعة. استخدم هذه الطريقة لإضافة سلاسل إلى مخططات Histogram. |
| [Clear](./clear/)() | يزيل جميع [ChartSeries](../chartseries/) من هذه المجموعة. |
| [get_Count](./get_count/)() | يعيد عدد [ChartSeries](../chartseries/) في هذه المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد [ChartSeries](../chartseries/) عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | يزيل [ChartSeries](../chartseries/) عند الفهرس المحدد. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية إضافة وإزالة بيانات السلاسل في مخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مخطط عمودي سيحتوي افتراضيًا على ثلاث سلاسل من بيانات تجريبية.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// كل سلسلة لها أربع قيم عشرية: واحدة لكل من الفئات الأربع.
// أربع مجموعات من ثلاثة أعمدة ستمثل هذه البيانات.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// اطبع اسم كل سلسلة في المخطط.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// هذه هي أسماء الفئات في المخطط.
System::ArrayPtr<System::String> categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// يمكننا إضافة سلسلة بقيم جديدة للفئات الموجودة.
// سيحتوي هذا المخطط الآن على أربع مجموعات من أربعة أعمدة.
chart->get_Series()->Add(u"Series 4", categories, System::MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// يمكن أيضًا إزالة سلسلة مخطط حسب الفهرس، مثل هذا.
// سيؤدي هذا إلى إزالة واحدة من السلاسل التجريبية الثلاث التي جاءت مع المخطط.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> s) -> bool
{
    return s->get_Name() == u"Series 3";
}))));

// يمكننا أيضًا مسح جميع بيانات المخطط مرة واحدة باستخدام هذه الطريقة.
// عند إنشاء مخطط جديد، هذه هي الطريقة لمسح جميع البيانات التجريبية
// قبل أن نتمكن من البدء في العمل على مخطط فارغ.
chartData->Clear();
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
