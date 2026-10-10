---
title: "Aspose::Words::Drawing::Charts::ChartXValueCollection فئة"
linktitle: "ChartXValueCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartXValueCollection فئة. تمثل مجموعة من قيم X لسلسلة مخطط في C++."
type: docs
weight: 18400
url: /ar/cpp/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class


يمثل مجموعة من قيم X لسلسلة المخطط.

```cpp
class ChartXValueCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() | يحصل على عدد العناصر في هذه المجموعة. |
| [get_FormatCode](./get_formatcode/)() | يحصل أو يضبط رمز التنسيق المطبق على قيم X. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يضبط قيمة X عند الفهرس المحدد. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | يحصل أو يضبط قيمة X عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## ملاحظات


يجب أن تكون جميع عناصر المجموعة باستثناء **null** لها نفس [ValueType](../chartxvalue/get_valuetype/).

تسمح المجموعة فقط بتغيير قيم X. لإضافة أو إدراج قيم جديدة إلى سلسلة مخطط، أو إزالة القيم، يمكن استخدام الأساليب المناسبة لفئة [ChartSeries](../chartseries/).

## أمثلة



يعرض كيفية الحصول على بيانات سلسلة المخطط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->idx_get(0);

double minValue = std::numeric_limits<double>::max();
int32_t minValueIndex = 0;
double maxValue = std::numeric_limits<double>::lowest();
int32_t maxValueIndex = 0;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    // امسح التنسيق الفردي لجميع نقاط البيانات.
    // نقاط البيانات وقيم البيانات هي واحد لواحد في المخططات العمودية.
    series->get_DataPoints()->idx_get(i)->ClearFormat();

    // احصل على قيمة Y.
    double yValue = series->get_YValues()->idx_get(i)->get_DoubleValue();

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// غيّر ألوان القيم القصوى والصغرى.
series->get_DataPoints()->idx_get(minValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series->get_DataPoints()->idx_get(maxValueIndex)->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Charts.GetChartSeriesData.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
