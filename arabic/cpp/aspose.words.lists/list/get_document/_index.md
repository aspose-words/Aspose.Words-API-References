---
title: "Aspose::Words::Lists::List::get_Document method"
linktitle: "get_Document"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Lists::List::get_Document method. يحصل على المستند المالِك في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.lists/list/get_document/
---
## List::get_Document method


يحصل على المستند المالِك.

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::Lists::List::get_Document() const
```

## ملاحظات


دائمًا ما تكون للقائمة مستند أبوي وتكون صالحة فقط في سياق ذلك المستند.

## أمثلة



يوضح كيفية التحقق من خصائص المستند المالك للقوائم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::ListCollection> lists = doc->get_Lists();
ASPOSE_ASSERT_EQ(doc, lists->get_Document());

System::SharedPtr<Aspose::Words::Lists::List> list = lists->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
ASPOSE_ASSERT_EQ(doc, list->get_Document());

std::cout << (System::String(u"Current list count: ") + lists->get_Count()) << std::endl;
std::cout << (System::String(u"Is the first document list: ") + (System::ObjectExt::Equals(lists->idx_get(0), list))) << std::endl;
std::cout << (System::String(u"ListId: ") + list->get_ListId()) << std::endl;
std::cout << (System::String(u"List is the same by ListId: ") + (System::ObjectExt::Equals(lists->GetListByListId(1), list))) << std::endl;
```

## انظر أيضًا

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
