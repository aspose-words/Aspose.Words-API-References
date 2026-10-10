---
title: "Aspose::Words::Markup::SdtAppearance enum"
linktitle: "SdtAppearance"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::SdtAppearance enum. يحدد مظهر علامة المستند المهيكلة في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.markup/sdtappearance/
---
## SdtAppearance enum


يحدد مظهر علامة المستند المهيكلة.

```cpp
enum class SdtAppearance
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| BoundingBox | 0 | يمثل علامة مستند مهيكلة تُعرض كمستطيل مظلل أو صندوق حدود. |
| العلامات | 1 | يمثل علامة مستند مهيكلة تُعرض كعلامات بداية ونهاية. |
| مخفي | 2 | يمثل علامة مستند مهيكلة غير معروضة. |
| Default | n/a | الإعداد الافتراضي هو [BoundingBox](./). |


## أمثلة



يوضح كيفية إظهار العلامة حول المحتوى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");
auto tag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

if (tag->get_Appearance() == Aspose::Words::Markup::SdtAppearance::Hidden)
{
    tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
