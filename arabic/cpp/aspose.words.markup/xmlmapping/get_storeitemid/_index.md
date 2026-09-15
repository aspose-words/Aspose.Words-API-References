---
title: "طريقة Aspose::Words::Markup::XmlMapping::get_StoreItemId"
linktitle: "get_StoreItemId"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::XmlMapping::get_StoreItemId. تحدد معرف بيانات XML المخصص لجزء البيانات XML المخصص الذي سيُستخدم لتقييم تعبير XPath في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.markup/xmlmapping/get_storeitemid/
---
## XmlMapping::get_StoreItemId method


تحدد معرف بيانات XML المخصص لجزء البيانات XML المخصص الذي سيُستخدم لتقييم تعبير [XPath](../get_xpath/).

```cpp
System::String Aspose::Words::Markup::XmlMapping::get_StoreItemId()
```


## أمثلة



يوضح كيفية الحصول على معرف بيانات XML المخصص لجزء XML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom XML part in structured document tag.docx");

// تحتوي العلامات المهيكلة للوثائق على معرفات بصيغة GUIDs.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 0, true));

ASSERT_EQ(u"{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag->get_XmlMapping()->get_StoreItemId());
```

## انظر أيضًا

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
