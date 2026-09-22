---
title: "طريقة Aspose::Words::Document::UnlinkFields"
linktitle: "UnlinkFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::UnlinkFields. يفك ارتباط الحقول في كامل المستند في C++."
type: docs
weight: 94000
url: /ar/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


يفك ارتباط الحقول في كامل المستند.

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## ملاحظات


يستبدل جميع الحقول في كامل المستند بأحدث نتائجها.

لفك ارتباط الحقول في جزء محدد من المستند استخدم [UnlinkFields](../../range/unlinkfields/).

## أمثلة



يعرض كيفية إلغاء ربط جميع الحقول في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
