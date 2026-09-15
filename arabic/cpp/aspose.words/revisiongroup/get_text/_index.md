---
title: "طريقة Aspose::Words::RevisionGroup::get_Text"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::RevisionGroup::get_Text. تُرجع النص المُدرج/المحذوف/المنقَل أو وصف تغيير التنسيق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


يرجع النص المُدرج/المحذوف/المنقَل أو وصف تغيير التنسيق.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
```


## أمثلة



يوضح كيفية طباعة معلومات حول مجموعة من المراجعات في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## انظر أيضًا

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
