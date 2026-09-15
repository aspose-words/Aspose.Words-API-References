---
title: "طريقة Aspose::Words::Range::UnlinkFields"
linktitle: "UnlinkFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Range::UnlinkFields. تفك ارتباط الحقول في هذا النطاق في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


يفك ربط الحقول في هذا النطاق.

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## ملاحظات


يستبدل جميع الحقول في هذا النطاق بأحدث نتائجها.

لفك ارتباط الحقول في المستند بأكمله استخدم [UnlinkFields](./).

## أمثلة



يعرض كيفية فك ارتباط جميع الحقول في نطاق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
