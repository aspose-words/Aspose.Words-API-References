---
title: "Aspose::Words::Fields::Field::GetFieldCode طريقة"
linktitle: "GetFieldCode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::Field::GetFieldCode طريقة. تُرجع النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.fields/field/getfieldcode/
---
## Field::GetFieldCode() method


يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل). يتم تضمين كل من شفرة الحقل ونتيجة الحقول الفرعية.

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode()
```


## أمثلة



يظهر كيفية إدراج حقل في مستند باستخدام رمز الحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدخلة.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```


يوضح كيفية الحصول على شفرة الحقل.
```cpp
// افتح مستندًا يحتوي على MERGEFIELD داخل حقل IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// هناك طريقتان للحصول على رمز حقل الحقل:
// 1 -  حذف الحقول الداخلية:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  تضمين الحقول الداخلية:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// بشكل افتراضي، تعرض طريقة GetFieldCode الحقول الداخلية.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
## Field::GetFieldCode(bool) method


يعيد النص بين بداية الحقل وفاصل الحقل (أو نهاية الحقل إذا لم يكن هناك فاصل).

```cpp
System::String Aspose::Words::Fields::Field::GetFieldCode(bool includeChildFieldCodes)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| includeChildFieldCodes | bool | **true** إذا كان يجب تضمين رموز الحقول الفرعية. |

## أمثلة



يوضح كيفية الحصول على شفرة الحقل.
```cpp
// افتح مستندًا يحتوي على MERGEFIELD داخل حقل IF.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Nested fields.docx");
auto fieldIf = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(doc->get_Range()->get_Fields()->idx_get(0));

// هناك طريقتان للحصول على رمز حقل الحقل:
// 1 -  حذف الحقول الداخلية:
ASSERT_EQ(u" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf->GetFieldCode(false));

// 2 -  تضمين الحقول الداخلية:
ASSERT_EQ(System::String::Format(u" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" "), fieldIf->GetFieldCode(true));

// بشكل افتراضي، تعرض طريقة GetFieldCode الحقول الداخلية.
ASSERT_EQ(fieldIf->GetFieldCode(), fieldIf->GetFieldCode(true));
```

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
