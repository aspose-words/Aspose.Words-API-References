---
title: "Aspose::Words::RevisionGroupCollection class"
linktitle: "RevisionGroupCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::RevisionGroupCollection class. مجموعة من كائنات RevisionGroup التي تمثل مجموعات المراجعة في المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 55000
url: /ar/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


مجموعة من كائنات [RevisionGroup](../revisiongroup/) التي تمثل مجموعات المراجعة في المستند. لمعرفة المزيد، زر مقالة الوثائق [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يعيد عدد مجموعات المراجعة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد مجموعة مراجعة في الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## ملاحظات


لا تقوم بإنشاء مثيلات من هذه الفئة مباشرة. استخدم الخاصية [Groups](../revisioncollection/get_groups/) للحصول على مجموعات المراجعة الموجودة في المستند.

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


يوضح كيفية الحصول على مجموعة من المراجعات في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
