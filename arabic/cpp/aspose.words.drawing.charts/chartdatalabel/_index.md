---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. يمثل تسمية البيانات على نقطة مخطط أو خط اتجاه. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


يمثل تسمية البيانات على نقطة مخطط أو خط اتجاه. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormat](./clearformat/)() | يمسح تنسيق هذه التسمية. يتم تعيين الخصائص إلى القيم الافتراضية المحددة في مجموعة تسميات البيانات الأصل. |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لهذه التسمية. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط لتسمية البيانات. |
| [get_Index](./get_index/)() | يحدد فهرس العنصر المحتوي. هذا الفهرس سيحدد أي من مجموعة عناصر الطفل للعنصر الأصل ينطبق عليه. القيمة الافتراضية هي 0. |
| [get_IsHidden](./get_ishidden/)() | يحصل/يضبط علامة تشير إلى ما إذا كانت هذه التسمية مخفية. القيمة الافتراضية هي **false**. |
| [get_IsVisible](./get_isvisible/)() | يرجع **true** إذا كانت هذه التسمية تحتوي على شيء للعرض. |
| [get_Left](./get_left/)() | يحصل أو يضبط المسافة (بالنقاط) لتسمية البيانات من الحافة اليسرى للمخطط أو من الموضع المحدد بخصية [Position](./get_position/) الخاصة به، اعتمادًا على قيمة خاصية [LeftMode](./get_leftmode/). |
| [get_LeftMode](./get_leftmode/)() | يحصل أو يضبط وضع تفسير قيمة خاصية [Left](./get_left/): سواء كان يحدد موقع تسمية البيانات من الحافة اليسرى للمخطط أو من الموضع المحدد بخصية [Position](./get_position/). |
| [get_NumberFormat](./get_numberformat/)() | يرجع تنسيق الرقم للعنصر الأصل. |
| [get_Orientation](./get_orientation/)() | يحصل أو يضبط اتجاه نص التسمية. |
| [get_Position](./get_position/)() | يحصل أو يضبط موضع تسمية البيانات. |
| [get_Rotation](./get_rotation/)() | يحصل أو يضبط دوران التسمية بالدرجات. |
| [get_Separator](./get_separator/)() | يحصل على الفاصل النصي المستخدم لتسميات البيانات في المخطط. القيمة الافتراضية هي فاصلة، باستثناء مخططات الفطيرة التي تعرض فقط اسم الفئة والنسبة المئوية، حيث يُستخدم فاصل سطر جديد بدلاً من ذلك. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | يسمح بتحديد ما إذا كان يجب عرض حجم الفقاعة لتسميات البيانات في المخطط. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | يسمح بتحديد ما إذا كان اسم الفئة سيُعرض لتسميات البيانات على المخطط. القيمة الافتراضية هي **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | يسمح بتحديد ما إذا كانت القيم من نطاق تسميات البيانات ستُعرض في تسميات البيانات. القيمة الافتراضية هي **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | يسمح بتحديد ما إذا كانت خطوط ربط تسميات البيانات تحتاج إلى العرض. القيمة الافتراضية هي **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | يسمح بتحديد ما إذا كان مفتاح الأسطورة سيُعرض لتسميات البيانات على المخطط. القيمة الافتراضية هي **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | يسمح بتحديد ما إذا كانت قيمة النسبة المئوية ستُعرض لتسميات البيانات على المخطط. القيمة الافتراضية هي **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | يعيد قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات على المخطط. **true** لعرض اسم السلسلة؛ **false** لإخفائه. القيمة الافتراضية هي **false**. |
| [get_ShowValue](./get_showvalue/)() | يسمح بتحديد ما إذا كانت القيم ستُعرض في تسميات البيانات. القيمة الافتراضية هي **false**. |
| [get_Top](./get_top/)() | يحصل أو يعيّن المسافة لتسمية البيانات بالنقاط من الحافة العليا للمخطط أو من الموضع المحدد بواسطة خاصية [Position](./get_position/) الخاصة به، اعتمادًا على قيمة خاصية [TopMode](./get_topmode/). |
| [get_TopMode](./get_topmode/)() | يحصل أو يعيّن وضع تفسير قيمة خاصية [Top](./get_top/): ما إذا كانت تحدد موقع تسمية البيانات من الحافة العليا للمخطط أو من الموضع المحدد بواسطة خاصية [Position](./get_position/) الخاصة به. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | يحصل/يضبط علامة تشير إلى ما إذا كانت هذه التسمية مخفية. القيمة الافتراضية هي **false**. |
| [set_Left](./set_left/)(double) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | يضبط فاصل السلسلة المستخدم لتسميات البيانات على المخطط. الافتراضي هو الفاصلة، باستثناء المخططات الدائرية التي تعرض فقط اسم الفئة والنسبة المئوية، حيث يُستخدم كسر السطر بدلاً من ذلك. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | يسمح بتحديد ما إذا كان اسم الفئة سيُعرض لتسميات البيانات على المخطط. القيمة الافتراضية هي **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | يسمح بتحديد ما إذا كانت القيم من نطاق تسميات البيانات ستُعرض في تسميات البيانات. القيمة الافتراضية هي **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | يسمح بتحديد ما إذا كانت خطوط ربط تسميات البيانات تحتاج إلى العرض. القيمة الافتراضية هي **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | يسمح بتحديد ما إذا كان مفتاح الأسطورة سيُعرض لتسميات البيانات على المخطط. القيمة الافتراضية هي **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | يسمح بتحديد ما إذا كانت قيمة النسبة المئوية ستُعرض لتسميات البيانات على المخطط. القيمة الافتراضية هي **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | يضبط قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات على المخطط. **true** لعرض اسم السلسلة؛ **false** لإخفائه. القيمة الافتراضية هي **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | يسمح بتحديد ما إذا كانت القيم ستُعرض في تسميات البيانات. القيمة الافتراضية هي **false**. |
| [set_Top](./set_top/)(double) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
