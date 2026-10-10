---
title: "واجهة Aspose::Words::Drawing::Charts::IChartDataPoint"
linktitle: "IChartDataPoint"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Drawing::Charts::IChartDataPoint. تحتوي على خصائص نقطة بيانات واحدة على المخطط في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


يحتوي على خصائص نقطة بيانات واحدة في المخطط.

```cpp
class IChartDataPoint : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات. |
| virtual [get_Explosion](./get_explosion/)() | يحدد مقدار إزاحة نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق أي انفجار. ينطبق فقط على مخططات الفطيرة. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| virtual [get_Marker](./get_marker/)() | يحدد علامة بيانات. يتم إنشاء العلامة تلقائيًا عند الطلب. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | المُعيّن لـ [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | المُعيّن لـ [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
