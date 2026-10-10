---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. يمثل مجموعة من أحجام الفقاعات لسلسلة مخطط في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


يمثل مجموعة أحجام الفقاعات لسلسلة مخطط.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Count](./get_count/)() | يحصل على عدد العناصر في هذه المجموعة. |
| [get_FormatCode](./get_formatcode/)() | يحصل أو يضبط رمز التنسيق المطبق على أحجام الفقاعات. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يضبط قيمة حجم الفقاعة عند المؤشر المحدد. |
| [idx_set](./idx_set/)(int32_t, double) | يحصل أو يضبط قيمة حجم الفقاعة عند المؤشر المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | محدد لـ [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## ملاحظات


تسمح المجموعة فقط بتغيير أحجام الفقاعات. لإضافة أو إدراج قيم جديدة إلى سلسلة مخطط، أو إزالة القيم، يمكن استخدام الأساليب المناسبة لفئة [ChartSeries](../chartseries/).

يتم تمثيل قيم أحجام الفقاعات الفارغة كـ **NaN**.

## انظر أيضًا

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
