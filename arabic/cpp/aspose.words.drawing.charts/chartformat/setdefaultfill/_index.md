---
title: "Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill طريقة"
linktitle: "SetDefaultFill"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill طريقة. يعيد تعيين تعبئة عنصر المخطط لتكون القيمة الافتراضية في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat::SetDefaultFill method


يعيد تعيين تعبئة عنصر المخطط إلى القيمة الافتراضية.

```cpp
void Aspose::Words::Drawing::Charts::ChartFormat::SetDefaultFill()
```


## أمثلة



يوضح كيفية إعادة تعيين التعبئة إلى القيمة الافتراضية المحددة في السلسلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DataPoint format.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = series->get_DataPoints()->idx_get(1);

ASSERT_TRUE(dataPoint->get_Format()->get_IsDefined());

dataPoint->get_Format()->SetDefaultFill();

doc->Save(get_ArtifactsDir() + u"Charts.ResetDataPointFill.docx");
```

## انظر أيضًا

* Class [ChartFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
