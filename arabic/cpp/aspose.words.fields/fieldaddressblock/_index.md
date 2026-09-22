---
title: "Aspose::Words::Fields::FieldAddressBlock class"
linktitle: "FieldAddressBlock"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldAddressBlock class. ينفّذ حقل ADDRESSBLOCK. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class


ينفذ الحقل ADDRESSBLOCK. لمعرفة المزيد، زر مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAddressBlock : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IFormattableMergeField
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [FieldAddressBlock](./fieldaddressblock/)() |  |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/)() | يحصل أو يعيّن اسم الدولة/المنطقة المستبعدة. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/)() | يحصل أو يعيّن ما إذا كان يجب تنسيق العنوان وفقًا لدولة/منطقة المستلم كما هو معرف بواسطة POST*CODE (الاتحاد البريدي العالمي 2006). |
| [get_IncludeCountryOrRegionName](./get_includecountryorregionname/)() | يحصل أو يعيّن ما إذا كان يجب تضمين اسم الدولة/المنطقة. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LanguageId](./get_languageid/)() | يحصل أو يعيّن معرف اللغة المستخدم لتنسيق العنوان. |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_NameAndAddressFormat](./get_nameandaddressformat/)() | يحصل أو يعيّن تنسيق الاسم والعنوان. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetFieldNames](./getfieldnames/)() override | يعيد مجموعة من أسماء حقول دمج البريد المستخدمة بواسطة الحقل. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_ExcludedCountryOrRegionName](./set_excludedcountryorregionname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/). |
| [set_FormatAddressOnCountryOrRegion](./set_formataddressoncountryorregion/)(bool) | مُعيّن لـ [Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/). |
| [set_IncludeCountryOrRegionName](./set_includecountryorregionname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldAddressBlock::get_IncludeCountryOrRegionName](./get_includecountryorregionname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldAddressBlock::get_LanguageId](./get_languageid/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NameAndAddressFormat](./set_nameandaddressformat/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat](./get_nameandaddressformat/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
