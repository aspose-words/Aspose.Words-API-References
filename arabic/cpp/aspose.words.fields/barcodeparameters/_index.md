---
title: "Aspose::Words::Fields::BarcodeParameters class"
linktitle: "BarcodeParameters"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::BarcodeParameters class. فئة حاوية لمعلمات الباركود لتمريرها إلى BarcodeGenerator. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.fields/barcodeparameters/
---
## BarcodeParameters class


فئة حاوية لمعلمات الباركود لتمريرها إلى BarcodeGenerator. لمعرفة المزيد، زر مقالة الوثائق [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class BarcodeParameters : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [BarcodeParameters](./barcodeparameters/)() |  |
| [get_AddStartStopChar](./get_addstartstopchar/)() const | ما إذا كان يجب إضافة أحرف البداية/النهاية لأنواع الباركود NW7 و CODE39. |
| [get_BackgroundColor](./get_backgroundcolor/)() const | لون خلفية الباركود (0x000000 - 0xFFFFFF) |
| [get_BarcodeType](./get_barcodetype/)() const | نوع الباركود. |
| [get_BarcodeValue](./get_barcodevalue/)() const | البيانات التي سيتم ترميزها. |
| [get_CaseCodeStyle](./get_casecodestyle/)() const | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [get_DisplayText](./get_displaytext/)() const | ما إذا كان يجب عرض بيانات الباركود (النص) مع الصورة. |
| [get_ErrorCorrectionLevel](./get_errorcorrectionlevel/)() const | مستوى تصحيح الأخطاء لرمز QR. القيم الصالحة هي [0, 3]. |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() const | نوع علامة التعريف المواجهة (FIM). |
| [get_FixCheckDigit](./get_fixcheckdigit/)() const | ما إذا كان يجب تصحيح رقم التحقق إذا كان غير صالح. |
| [get_ForegroundColor](./get_foregroundcolor/)() const | لون المقدمة للباركود (0x000000 - 0xFFFFFF) |
| [get_IsBookmark](./get_isbookmark/)() const | ما إذا كان [PostalAddress](./get_postaladdress/) هو اسم إشارة مرجعية. |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() const | ما إذا كان [PostalAddress](./get_postaladdress/) عنوانًا بريديًا أمريكيًا. |
| [get_PosCodeStyle](./get_poscodestyle/)() const | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [get_PostalAddress](./get_postaladdress/)() const | عنوان البريد للباركود. |
| [get_ScalingFactor](./get_scalingfactor/)() const | عامل التحجيم للرمز. القيمة بوحدات النسبة المئوية الكاملة والقيم الصالحة هي [10, 1000]. |
| [get_SymbolHeight](./get_symbolheight/)() const | ارتفاع صورة الباركود (بالـ twips - 1/1440 بوصة) |
| [get_SymbolRotation](./get_symbolrotation/)() const | دوران رمز الباركود. القيم الصالحة هي [0, 3]. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddStartStopChar](./set_addstartstopchar/)(bool) | ما إذا كان يجب إضافة أحرف البداية/النهاية لأنواع الباركود NW7 و CODE39. |
| [set_BackgroundColor](./set_backgroundcolor/)(const System::String\&) | لون خلفية الباركود (0x000000 - 0xFFFFFF) |
| [set_BarcodeType](./set_barcodetype/)(const System::String\&) | نوع الباركود. |
| [set_BarcodeValue](./set_barcodevalue/)(const System::String\&) | البيانات التي سيتم ترميزها. |
| [set_CaseCodeStyle](./set_casecodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Case Code for barcode type ITF14. The valid values are [STD | EXT | ADD]. |
| [set_DisplayText](./set_displaytext/)(bool) | ما إذا كان يجب عرض بيانات الباركود (النص) مع الصورة. |
| [set_ErrorCorrectionLevel](./set_errorcorrectionlevel/)(const System::String\&) | مستوى تصحيح الأخطاء لرمز QR. القيم الصالحة هي [0, 3]. |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | نوع علامة التعريف المواجهة (FIM). |
| [set_FixCheckDigit](./set_fixcheckdigit/)(bool) | ما إذا كان يجب تصحيح رقم التحقق إذا كان غير صالح. |
| [set_ForegroundColor](./set_foregroundcolor/)(const System::String\&) | لون المقدمة للباركود (0x000000 - 0xFFFFFF) |
| [set_IsBookmark](./set_isbookmark/)(bool) | ما إذا كان [PostalAddress](./get_postaladdress/) هو اسم إشارة مرجعية. |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | ما إذا كان [PostalAddress](./get_postaladdress/) عنوانًا بريديًا أمريكيًا. |
| [set_PosCodeStyle](./set_poscodestyle/)(const System::String\&) | [Style](../../aspose.words/style/) of a Point of Sale barcode (barcode types UPCA | UPCE | EAN13 | EAN8). The valid values (case insensitive) are [STD | SUP2 | SUP5 | CASE]. |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | عنوان البريد للباركود. |
| [set_ScalingFactor](./set_scalingfactor/)(const System::String\&) | عامل التحجيم للرمز. القيمة بوحدات النسبة المئوية الكاملة والقيم الصالحة هي [10, 1000]. |
| [set_SymbolHeight](./set_symbolheight/)(const System::String\&) | ارتفاع صورة الباركود (بالـ twips - 1/1440 بوصة) |
| [set_SymbolRotation](./set_symbolrotation/)(const System::String\&) | دوران رمز الباركود. القيم الصالحة هي [0, 3]. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
