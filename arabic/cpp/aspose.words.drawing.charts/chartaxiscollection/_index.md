---
title: "Aspose::Words::Drawing::Charts::ChartAxisCollection class"
linktitle: "ChartAxisCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisCollection class. يمثل مجموعة من محاور المخطط في C++."
type: docs
weight: 5500
url: /ar/cpp/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class


يمثل مجموعة محاور المخطط.

```cpp
class ChartAxisCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() | يحصل على عدد المحاور في هذه المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل على المحور عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية العمل مع مجموعة المحاور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// إخفاء خطوط الشبكة الرئيسية على المحاور Y الأساسية والثانوية.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
