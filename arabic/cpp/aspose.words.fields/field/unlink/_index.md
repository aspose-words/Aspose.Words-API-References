---
title: "Aspose::Words::Fields::Field::Unlink طريقة"
linktitle: "إلغاء الارتباط"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::Field::Unlink. تقوم بتنفيذ إلغاء ربط الحقل في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


ينفّذ فك ربط الحقل.

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## ملاحظات


يستبدل الحقل بأحدث نتيجة له.

بعض الحقول، مثل حقول XE (إدخال الفهرس) وحقول SEQ (التسلسل)، لا يمكن إلغاء ربطها.

## أمثلة



يعرض كيفية إلغاء ربط حقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
