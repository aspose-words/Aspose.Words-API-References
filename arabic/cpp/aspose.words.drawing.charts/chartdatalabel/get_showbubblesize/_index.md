---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize طريقة"
linktitle: "get_ShowBubbleSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize طريقة. يسمح بتحديد ما إذا كان يجب عرض حجم الفقاعات لتسميات البيانات على المخطط. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي false في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabel/get_showbubblesize/
---
## ChartDataLabel::get_ShowBubbleSize method


يسمح بتحديد ما إذا كان يجب عرض حجم الفقاعة لتسميات البيانات في المخطط. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize()
```


## أمثلة



يوضح كيفية استخدام التأثيرات ثلاثية الأبعاد مع مخططات الفقاعات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// طبق تسمية بيانات على كل فقاعة تُظهر قطرها.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## انظر أيضًا

* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
