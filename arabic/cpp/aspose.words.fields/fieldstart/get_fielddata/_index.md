---
title: "طريقة get_FieldData في Aspose::Words::Fields::FieldStart"
linktitle: "get_FieldData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة get_FieldData في Aspose::Words::Fields::FieldStart. تحصل على بيانات الحقل المخصصة المرتبطة بالحقل في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


يحصل على بيانات الحقل المخصصة المرتبطة بالحقل.

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## أمثلة



يظهر كيفية الحصول على البيانات المرتبطة بالحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## انظر أيضًا

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
