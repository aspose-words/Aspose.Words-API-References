---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint فئة"
linktitle: "ChartDataPoint"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint فئة. يسمح بتحديد تنسيق نقطة بيانات واحدة على المخطط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


يسمح بتحديد تنسيق نقطة بيانات واحدة على المخطط. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormat](./clearformat/)() | يمسح تنسيق هذه النقطة البيانات. يتم ضبط الخصائص إلى القيم الافتراضية المعرفة في السلسلة الأم. |
| [get_Bubble3D](./get_bubble3d/)() override | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات. |
| [get_Explosion](./get_explosion/)() override | يحدد مقدار إزاحة نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق أي انفجار. ينطبق فقط على مخططات الفطيرة. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط لهذه النقطة البيانات. |
| [get_Index](./get_index/)() | فهرس نقطة البيانات التي يطبق هذا الكائن تنسيقها عليها. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| [get_Marker](./get_marker/)() override | يحدد علامة بيانات المخطط. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات. |
| [set_Explosion](./set_explosion/)(int32_t) override | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
