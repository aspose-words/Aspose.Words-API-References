---
title: "Aspose::Words::Lists::ListCollection::GetListByListId method"
linktitle: "GetListByListId"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListCollection::GetListByListId. تحصل على قائمة بواسطة معرف القائمة في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection::GetListByListId method


يحصل على قائمة باستخدام معرف القائمة.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::GetListByListId(int32_t listId)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| listId | int32_t | معرف القائمة. |

### ReturnValue

يرجع كائن القائمة. يرجع **null** إذا لم يتم العثور على قائمة بالمعرف المحدد.
## ملاحظات


عادةً لا تحتاج إلى استخدام هذه الطريقة. في معظم الأوقات تقوم بتطبيق تنسيق القائمة على الفقرات فقط عن طريق ضبط خاصية [List](../../listformat/get_list/) لكائن [ListFormat](../../listformat/).

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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
