---
title: "Aspose::Words::BookmarkCollection class"
linktitle: "BookmarkCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BookmarkCollection class. مجموعة من كائنات Bookmark التي تمثل الإشارات المرجعية في النطاق المحدد. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/bookmarkcollection/
---
## BookmarkCollection class


مجموعة من كائنات [Bookmark](../bookmark/) التي تمثل الإشارات المرجعية في النطاق المحدد. لمعرفة المزيد، زر مقالة الوثائق [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarkCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bookmark>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Clear](./clear/)() | يزيل جميع الإشارات المرجعية من هذه المجموعة ومن المستند. |
| [get_Count](./get_count/)() | يعيد عدد العلامات المرجعية في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عدّاد. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يعيد علامة مرجعية في الفهرس المحدد. |
| [idx_get](./idx_get/)(const System::String\&) | يعيد علامة مرجعية بالاسم. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Bookmark\>\&) | يزيل العلامة المرجعية المحددة من المستند. |
| [Remove](./remove/)(const System::String\&) | يزيل علامة مرجعية بالاسم المحدد. |
| [RemoveAt](./removeat/)(int32_t) | يزيل علامة مرجعية في الفهرس المحدد. |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
