---
title: "طريقة Aspose::Words::RevisionGroup::get_RevisionType"
linktitle: "get_RevisionType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::RevisionGroup::get_RevisionType. يحصل على نوع التعديلات المتضمنة في هذه المجموعة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/revisiongroup/get_revisiontype/
---
## RevisionGroup::get_RevisionType method


يحصل على نوع المراجعات المتضمنة في هذه المجموعة.

```cpp
Aspose::Words::RevisionType Aspose::Words::RevisionGroup::get_RevisionType()
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

* Enum [RevisionType](../../revisiontype/)
* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
