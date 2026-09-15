---
title: "Aspose::Words::Drawing::Charts::ChartYValue فئة"
linktitle: "ChartYValue"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::ChartYValue فئة. يمثل قيمة Y لسلسلة مخطط في C++."
type: docs
weight: 18600
url: /ar/cpp/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class


يمثل قيمة Y لسلسلة مخطط.

```cpp
class ChartYValue : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | يحصل على علم يشير إلى ما إذا كان الكائن المحدد يساوي كائن قيمة Y الحالي. |
| static [FromDateTime](./fromdatetime/)(System::DateTime) | ينشئ مثيلًا من [ChartYValue](./) من نوع [DateTime](../chartyvaluetype/). |
| static [FromDouble](./fromdouble/)(double) | ينشئ مثيلًا من [ChartYValue](./) من نوع [Double](../chartyvaluetype/). |
| static [FromTimeSpan](./fromtimespan/)(System::TimeSpan) | ينشئ مثيلًا من [ChartYValue](./) من نوع [Time](../chartyvaluetype/). |
| [get_DateTimeValue](./get_datetimevalue/)() const | يحصل على قيمة التاريخ والوقت المخزنة. |
| [get_DoubleValue](./get_doublevalue/)() const | يحصل على القيمة الرقمية المخزنة. |
| [get_TimeValue](./get_timevalue/)() const | يحصل على قيمة الوقت المخزنة. |
| [get_ValueType](./get_valuetype/)() const | يحصل على نوع قيمة Y المخزنة في الكائن. |
| [GetHashCode](./gethashcode/)() const override | يحصل على رمز تجزئة لكائن قيمة Y الحالي. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


تحتوي هذه الفئة على عدد من الطرق الساكنة لإنشاء قيمة Y من نوع معين. تسمح الخاصية [ValueType](./get_valuetype/) لك بتحديد نوع قيمة Y موجودة.

يجب أن تكون جميع قيم Y غير الفارغة لسلسلة مخطط من نفس نوع [ChartYValueType](../chartyvaluetype/).
## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
