---
title: "طريقة Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom"
linktitle: "CopyFormatFrom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom. تنسخ تنسيق نقطة البيانات الافتراضي من نقطة البيانات ذات الفهرس المحدد في C++."
type: docs
weight: 1875
url: /ar/cpp/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries::CopyFormatFrom method


ينسخ تنسيق نقطة البيانات الافتراضي من نقطة البيانات ذات الفهرس المحدد.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::CopyFormatFrom(int32_t dataPointIndex)
```


## أمثلة



يعرض كيفية نسخ تنسيق نقطة البيانات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

// احصل على المخطط والسلسلة لتحديث التنسيق.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPointCollection> dataPoints = series->get_DataPoints();

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_FALSE(dataPoints->HasDefaultFormat(1));

// نسخ تنسيق نقطة البيانات ذات الفهرس 1 إلى نقطة البيانات ذات الفهرس 2
// بحيث تبدو نقطة البيانات 2 مماثلة لنقطة البيانات 1.
dataPoints->CopyFormat(0, 1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

// انسخ تنسيق نقطة البيانات ذات الفهرس 0 إلى الإعدادات الافتراضية للسلسلة بحيث تكون جميع نقاط البيانات
// في السلسلة التي لديها التنسيق الافتراضي تبدو مثل نقطة البيانات 0.
series->CopyFormatFrom(1);

ASSERT_TRUE(dataPoints->HasDefaultFormat(0));
ASSERT_TRUE(dataPoints->HasDefaultFormat(1));

doc->Save(get_ArtifactsDir() + u"Charts.CopyDataPointFormat.docx");
```

## انظر أيضًا

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
