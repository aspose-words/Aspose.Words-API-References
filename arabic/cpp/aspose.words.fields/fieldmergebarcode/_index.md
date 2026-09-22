---
title: "Aspose::Words::Fields::FieldMergeBarcode فئة"
linktitle: "FieldMergeBarcode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldMergeBarcode فئة. تنفّذ حقل MERGEBARCODE. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 66000
url: /ar/cpp/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class


ينفذ حقل MERGEBARCODE. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeBarcode : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IMergeFieldSurrogate
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_AddStartStopChar](./get_addstartstopchar/)() | يحصل على ما إذا كان يجب إضافة أحرف البداية/النهاية لأنواع الباركود NW7 و CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() | يحصل على لون الخلفية لرمز الباركود. القيم الصالحة تكون في النطاق [0, 0xFFFFFF]. |
| [get_BarcodeType](./get_barcodetype/)() | يحصل على نوع الباركود (QR، إلخ). |
| [get_BarcodeValue](./get_barcodevalue/)() | يحصل على قيمة الباركود. |
| [get_CaseCodeStyle](./get_casecodestyle/)() | Gets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayResult](../field/get_displayresult/)() | يحصل على النص الذي يمثل نتيجة الحقل المعروضة. |
| [get_DisplayText](./get_displaytext/)() | يحصل على ما إذا كان يجب عرض بيانات الباركود (النص) مع الصورة. |
| [get_End](./get_end/)() override | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_End](../field/get_end/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() | يحصل على مستوى تصحيح الأخطاء لرمز QR. القيم الصالحة هي [0, 3]. |
| [get_FieldEnd](../field/get_fieldend/)() const | يحصل على العقدة التي تمثل نهاية الحقل. |
| [get_FieldStart](../field/get_fieldstart/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_FixCheckDigit](./get_fixcheckdigit/)() | يحصل على ما إذا كان يجب تصحيح رقم التحقق إذا كان غير صالح. |
| [get_ForegroundColor](./get_foregroundcolor/)() | يحصل على لون المقدمة لرمز الباركود. القيم الصالحة تكون في النطاق [0, 0xFFFFFF]. |
| [get_Format](../field/get_format/)() | يحصل على كائن [FieldFormat](../fieldformat/) الذي يوفّر وصولًا من نوع إلى تنسيق الحقل. |
| [get_IsDirty](../field/get_isdirty/)() | يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند. |
| [get_IsLocked](../field/get_islocked/)() | يحصل أو يعيّن ما إذا كان الحقل مقفلًا (يجب عدم إعادة حساب نتيجته). |
| [get_LocaleId](../field/get_localeid/)() | يحصل أو يعيّن معرف اللغة (LCID) للحقل. |
| [get_PosCodeStyle](./get_poscodestyle/)() | Gets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_Result](../field/get_result/)() | يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل. |
| [get_ScalingFactor](./get_scalingfactor/)() | يحصل على عامل التحجيم للرمز. القيمة بوحدات النسبة المئوية الكاملة والقيم الصالحة هي [10, 1000]. |
| [get_Separator](./get_separator/)() override | يحصل على العقدة التي تمثل فاصل الحقل. يمكن أن تكون **null**. |
| [get_Start](./get_start/)() override | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_Start](../field/get_start/)() const | يحصل على العقدة التي تمثل بداية الحقل. |
| [get_SymbolHeight](./get_symbolheight/)() | يحصل على ارتفاع الرمز. الوحدات هي TWIPS (1/1440 بوصة). |
| [get_SymbolRotation](./get_symbolrotation/)() | يحصل على دوران رمز الباركود. القيم الصالحة هي [0, 3]. |
| virtual [get_Type](../field/get_type/)() const | يحصل على نوع حقل Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية. |
| [GetFieldCode](../field/getfieldcode/)(bool) | يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | يزيل الحقل من المستند. يعيد عقدة مباشرةً بعد الحقل. إذا كانت نهاية الحقل هي الطفل الأخير لعقدة الوالد، يعيد الفقرة الأم. إذا كان الحقل قد أُزيل بالفعل، يعيد **null**. |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | يضبط ما إذا كان يجب إضافة أحرف البداية/النهاية لأنواع الباركود NW7 و CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | يضبط لون الخلفية لرمز الباركود. القيم الصالحة تكون في النطاق [0, 0xFFFFFF]. |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | يضبط نوع الباركود (QR، إلخ). |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | يضبط قيمة الباركود. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | Sets the style of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | يضبط ما إذا كان يجب عرض بيانات الباركود (النص) مع الصورة. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | يضبط مستوى تصحيح الأخطاء لرمز QR. القيم الصالحة هي [0, 3]. |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | يضبط ما إذا كان يجب تصحيح رقم التحقق إذا كان غير صالح. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | يضبط لون المقدمة لرمز الباركود. القيم الصالحة تكون في النطاق [0, 0xFFFFFF]. |
| [set_IsDirty](../field/set_isdirty/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | مُعيّن لـ [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | مُعيّن لـ [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | Sets the style of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_Result](../field/set_result/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | يضبط عامل التحجيم للرمز. القيمة بوحدات النسبة المئوية الكاملة والقيم الصالحة هي [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | يضبط ارتفاع الرمز. الوحدات هي TWIPS (1/1440 بوصة). |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | يضبط دوران رمز الباركود. القيم الصالحة هي [0, 3]. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | ينفّذ فك ربط الحقل. |
| [Update](../field/update/)() | ينفّذ تحديث الحقل. يطرح استثناءً إذا كان الحقل قيد التحديث بالفعل. |
| [Update](../field/update/)(bool) | يقوم بتنفيذ تحديث الحقل. يُطلق استثناء إذا كان الحقل قيد التحديث بالفعل. |
## انظر أيضًا

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
