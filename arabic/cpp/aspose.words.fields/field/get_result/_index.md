---
title: "Aspose::Words::Fields::Field::get_Result طريقة"
linktitle: "get_Result"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::Field::get_Result. يحصل على النص أو يضبطه الذي يقع بين فاصل الحقل ونهاية الحقل في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.fields/field/get_result/
---
## Field::get_Result method


يحصل أو يعيّن النص الموجود بين فاصل الحقل ونهاية الحقل.

```cpp
System::String Aspose::Words::Fields::Field::get_Result()
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

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
