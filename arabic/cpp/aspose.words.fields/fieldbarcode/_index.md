---
title: "Aspose::Words::Fields::FieldBarcode class"
linktitle: "FieldBarcode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldBarcode class. ينفذ حقل BARCODE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class


يُنفّذ حقل BARCODE. لمزيد من المعلومات، زر [العمل مع الحقول](https://docs.aspose.com/words/cpp/working-with-fields/) مقالة الوثائق.

```cpp
class FieldBarcode : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() | يحصل أو يعيّن نوع علامة التعريف المواجهة (FIM) للإدراج. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsBookmark](./get_isbookmark/)() | يحصل أو يعيّن ما إذا كان [PostalAddress](./get_postaladdress/) هو اسم إشارة مرجعية. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() | يحصل أو يعيّن ما إذا كان [PostalAddress](./get_postaladdress/) عنوانًا بريديًا أمريكيًا. |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_PostalAddress](./get_postaladdress/)() | يحصل أو يعيّن العنوان البريدي المستخدم لإنشاء رمز شريطي أو اسم الإشارة المرجعية التي تشير إليه. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_Separator](../field/get_separator/)() | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | محدد لـ [Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark](./get_facingidentificationmark/). |
| [set_IsBookmark](./set_isbookmark/)(bool) | محدد لـ [Aspose::Words::Fields::FieldBarcode::get_IsBookmark](./get_isbookmark/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | محدد لـ [Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress](./get_isuspostaladdress/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | محدد لـ [Aspose::Words::Fields::FieldBarcode::get_PostalAddress](./get_postaladdress/). |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |

## أمثلة



يظهر كيفية استخدام حقل BARCODE لعرض رموز ZIP الأمريكية على شكل رمز شريطي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// فيما يلي طريقتان لاستخدام حقول BARCODE لعرض قيم مخصصة كرموز شريطية.
// 1 - احفظ القيمة التي سيعرضها الباركود في الخاصية PostalAddress:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// يجب أن تكون هذه القيمة رمز ZIP صالح.
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 - إشارة إلى إشارة مرجعية تخزن القيمة التي سيعرضها هذا الباركود:
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// الإشارة المرجعية التي يشير إليها حقل BARCODE في خاصية PostalAddress الخاصة به
// يجب أن تحتوي فقط على رمز ZIP صالح.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
