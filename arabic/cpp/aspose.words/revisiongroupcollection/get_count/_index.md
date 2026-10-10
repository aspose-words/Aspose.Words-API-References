---
title: "طريقة Aspose::Words::RevisionGroupCollection::get_Count"
linktitle: "get_Count"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::RevisionGroupCollection::get_Count. تُرجِع عدد مجموعات المراجعة في المجموعة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


يعيد عدد مجموعات المراجعة في المجموعة.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
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

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
