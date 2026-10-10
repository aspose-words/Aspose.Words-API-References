---
title: "فئة Aspose::Words::Bookmark"
linktitle: "إشارة مرجعية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Bookmark. تمثل إشارة مرجعية واحدة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/bookmark/
---
## Bookmark class


يمثل علامة مرجعية واحدة. لمعرفة المزيد، زر مقالة الوثائق [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class Bookmark : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BookmarkEnd](./get_bookmarkend/)() | يحصل على العقدة التي تمثل نهاية الإشارة المرجعية. |
| [get_BookmarkStart](./get_bookmarkstart/)() const | يحصل على العقدة التي تمثل بداية الإشارة المرجعية. |
| [get_FirstColumn](./get_firstcolumn/)() | يحصل على الفهرس الصفري للعمود الأول من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية. |
| [get_IsColumn](./get_iscolumn/)() | يرجع **true** إذا كانت هذه الإشارة المرجعية إشارة عمود جدول. |
| [get_LastColumn](./get_lastcolumn/)() | يحصل على الفهرس الصفري للعمود الأخير من نطاق أعمدة الجدول المرتبط بالإشارة المرجعية. |
| [get_Name](./get_name/)() | يحصل أو يعيّن اسم الإشارة المرجعية. |
| [get_Text](./get_text/)() | يحصل على النص المحاط بالإشارة المرجعية. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل الإشارة المرجعية من المستند. لا يزيل النص داخل الإشارة المرجعية. |
| [set_Name](./set_name/)(const System::String\&) | المُعيّن لـ [Aspose::Words::Bookmark::get_Name](./get_name/). |
| [set_Text](./set_text/)(const System::String\&) | يعيّن النص المحاط بالإشارة المرجعية. |
| static [Type](./type/)() |  |
## ملاحظات


[Bookmark](./) is a "facade" object that encapsulates two nodes [BookmarkStart](./get_bookmarkstart/) and [BookmarkEnd](./get_bookmarkend/) in a document tree and allows to work with a bookmark as a single object. 
## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
