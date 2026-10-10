---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel طريقة"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel method. يحصل على أو يضبط اسم معرف التسلسل المستخدم عند بناء جدول الأشكال الذي لا يتضمن تسمية ورقم التسمية التوضيحية في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


يحصل أو يحدد اسم معرف التسلسل المستخدم عند إنشاء جدول الأشكال الذي لا يتضمن تسمية ورقم التسمية التوضيحية.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## أمثلة



يظهر كيفية ضبط اسم معرف التسلسل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## انظر أيضًا

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
