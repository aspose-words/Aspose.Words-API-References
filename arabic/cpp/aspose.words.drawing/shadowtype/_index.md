---
title: "Aspose::Words::Drawing::ShadowType تعداد"
linktitle: "ShadowType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShadowType تعداد. يحدد نوع ظل الشكل في C++."
type: docs
weight: 35000
url: /ar/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


يحدد نوع ظل الشكل.

```cpp
enum class ShadowType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| ShadowMixed | -2 | لا أحد من إعدادات الظل المحددة مسبقًا. |
| Shadow1 | 1 | نوع الظل الأول. |
| Shadow10 | 10 | النوع العاشر للظل. |
| Shadow11 | 11 | النوع الحادي عشر للظل. |
| Shadow12 | 12 | النوع الثاني عشر للظل. |
| Shadow13 | 13 | النوع الثالث عشر للظل. |
| Shadow14 | 14 | النوع الرابع عشر للظل. |
| Shadow15 | 15 | النوع الخامس عشر للظل. |
| Shadow16 | 16 | النوع السادس عشر للظل. |
| Shadow17 | 17 | النوع السابع عشر للظل. |
| Shadow18 | 18 | النوع الثامن عشر للظل. |
| Shadow19 | 19 | النوع التاسع عشر للظل. |
| Shadow2 | 2 | النوع الثاني للظل. |
| Shadow20 | 20 | النوع العشرون للظل. |
| Shadow21 | 21 | النوع الحادي والعشرون للظل. |
| Shadow22 | 22 | نوع الظل الثاني والعشرون. |
| Shadow23 | 23 | نوع الظل الثالث والعشرون. |
| Shadow24 | 24 | نوع الظل الرابع والعشرون. |
| Shadow25 | 25 | نوع الظل الخامس والعشرون. |
| Shadow26 | 26 | نوع الظل السادس والعشرون. |
| Shadow27 | 27 | نوع الظل السابع والعشرون. |
| Shadow28 | 28 | نوع الظل الثامن والعشرون. |
| Shadow29 | 29 | نوع الظل التاسع والعشرون. |
| Shadow3 | 3 | نوع الظل الثالث. |
| Shadow30 | 30 | نوع الظل الثلاثون. |
| Shadow31 | 31 | نوع الظل الواحد والثلاثون. |
| Shadow32 | 32 | نوع الظل الثاني والثلاثون. |
| Shadow33 | 33 | نوع الظل الثالث والثلاثون. |
| ظل34 | 34 | نوع الظل الرابع والثلاثون. |
| ظل35 | 35 | نوع الظل الخامس والثلاثون. |
| ظل36 | 36 | نوع الظل السادس والثلاثون. |
| ظل37 | 37 | نوع الظل السابع والثلاثون. |
| ظل38 | 38 | نوع الظل الثامن والثلاثون. |
| ظل39 | 39 | نوع الظل التاسع والثلاثون. |
| ظل4 | 4 | نوع الظل الرابع. |
| ظل40 | 40 | نوع الظل الأربعون. |
| ظل41 | 41 | نوع الظل الحادي والأربعون. |
| ظل42 | 42 | نوع الظل الثاني والأربعون. |
| ظل43 | 43 | نوع الظل الثالث والأربعون. |
| ظل5 | 5 | نوع الظل الخامس. |
| Shadow6 | 6 | النوع الظل السادس. |
| Shadow7 | 7 | النوع الظل السابع. |
| Shadow8 | 8 | النوع الظل الثامن. |
| Shadow9 | 9 | النوع الظل التاسع. |


## أمثلة



يعرض كيفية العمل مع تنسيق الظل للشكل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
