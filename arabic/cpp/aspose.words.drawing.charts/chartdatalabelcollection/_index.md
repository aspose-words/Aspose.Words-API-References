---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class"
linktitle: "ChartDataLabelCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection class. يمثل مجموعة من ChartDataLabel. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


يمثل مجموعة من [ChartDataLabel](../chartdatalabel/). لمعرفة المزيد، زر مقالة الوثائق [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormat](./clearformat/)() | يمسح تنسيق جميع [ChartDataLabel](../chartdatalabel/) في هذه المجموعة. |
| [get_Count](./get_count/)() | يعيد عدد [ChartDataLabel](../chartdatalabel/) في هذه المجموعة. |
| [get_Font](./get_font/)() | يوفر الوصول إلى تنسيق الخط لتسميات البيانات للسلسلة بأكملها. |
| [get_Format](./get_format/)() | يوفر الوصول إلى تنسيق التعبئة والخط لتسميات البيانات. |
| [get_NumberFormat](./get_numberformat/)() | يحصل على كائن [ChartNumberFormat](../chartnumberformat/) يتيح تعيين تنسيق الأرقام لتسميات البيانات للسلسلة بأكملها. |
| [get_Orientation](./get_orientation/)() | يحصل أو يضبط اتجاه النص لتسميات البيانات للسلسلة بأكملها. |
| [get_Position](./get_position/)() | يحصل أو يضبط موضع تسميات البيانات. |
| [get_Rotation](./get_rotation/)() | يحصل أو يضبط دوران تسميات البيانات للسلسلة بأكملها بالدرجات. |
| [get_Separator](./get_separator/)() | يحصل أو يضبط الفاصل النصي المستخدم لتسميات البيانات للسلسلة بأكملها. الافتراضي هو الفاصلة، باستثناء المخططات الدائرية التي تعرض فقط اسم الفئة والنسبة المئوية، حيث يُستخدم كسر السطر بدلاً من ذلك. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | يسمح بتحديد ما إذا كان يجب عرض حجم الفقاعات لتسميات البيانات للسلسلة بأكملها. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | يسمح بتحديد ما إذا كان يجب عرض اسم الفئة لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | يسمح بتحديد ما إذا كان يجب عرض القيم من نطاق تسميات البيانات في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | يسمح بتحديد ما إذا كان يجب إظهار خطوط القائد لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | يسمح بتحديد ما إذا كان يجب عرض مفتاح الأسطورة لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | يسمح بتحديد ما إذا كان يجب عرض القيمة النسبية لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. ينطبق فقط على المخططات الدائرية. |
| [get_ShowSeriesName](./get_showseriesname/)() | يعيد أو يضبط قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات للسلسلة بأكملها. **true** لإظهار اسم السلسلة؛ **false** لإخفائه. بشكل افتراضي **false**. |
| [get_ShowValue](./get_showvalue/)() | يسمح بتحديد ما إذا كان يجب عرض القيم في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد [ChartDataLabel](../chartdatalabel/) للمؤشر المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | دالة تعيين لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | يسمح بتحديد ما إذا كان يجب عرض القيم من نطاق تسميات البيانات في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | مُعيّن لـ [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
