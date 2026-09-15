---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::RevisionGroup class. يمثل مجموعة من كائنات Revision المتسلسلة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 54000
url: /ar/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


يمثل مجموعة من كائنات [Revision](../revision/) المتسلسلة. لمعرفة المزيد، زر مقالة الوثائق [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Author](./get_author/)() | يحصل على مؤلف مجموعة المراجعات هذه. |
| [get_RevisionType](./get_revisiontype/)() | يحصل على نوع المراجعات المتضمنة في هذه المجموعة. |
| [get_Text](./get_text/)() | يرجع النص المُدرج/المحذوف/المنقَل أو وصف تغيير التنسيق. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
