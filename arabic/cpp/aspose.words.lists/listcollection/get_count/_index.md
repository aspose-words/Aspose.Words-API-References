---
title: "Aspose::Words::Lists::ListCollection::get_Count method"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListCollection::get_Count. تحصل على عدد القوائم المرقمة والقوائم ذات النقاط في المستند في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.lists/listcollection/get_count/
---
## ListCollection::get_Count method


يحصل على عدد القوائم المرقمة والنقطية في المستند.

```cpp
int32_t Aspose::Words::Lists::ListCollection::get_Count()
```


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

* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
