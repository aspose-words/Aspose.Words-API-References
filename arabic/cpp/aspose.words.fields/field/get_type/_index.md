---
title: "طريقة Aspose::Words::Fields::Field::get_Type"
linktitle: "get_Type"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::Field::get_Type. يحصل على نوع حقل Microsoft Word في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.fields/field/get_type/
---
## Field::get_Type method


يحصل على نوع حقل Microsoft Word.

```cpp
virtual Aspose::Words::Fields::FieldType Aspose::Words::Fields::Field::get_Type() const
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

* Enum [FieldType](../../fieldtype/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
