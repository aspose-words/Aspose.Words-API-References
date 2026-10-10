---
title: "طريقة Aspose::Words::Bookmark::get_Name"
linktitle: "get_Name"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Bookmark::get_Name. يحصل على اسم العلامة المرجعية أو يضبطه في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/bookmark/get_name/
---
## Bookmark::get_Name method


يحصل أو يعيّن اسم الإشارة المرجعية.

```cpp
System::String Aspose::Words::Bookmark::get_Name()
```


## أمثلة



يظهر كيفية إدراج علامة مرجعية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// العلامة المرجعية الصالحة لها اسم وعقدة BookmarkStart وعقدة BookmarkEnd.
// أي مسافة بيضاء في أسماء العلامات المرجعية ستحول إلى شرطات سفلية إذا فتحنا المستند المحفوظ باستخدام Microsoft Word.
// إذا قمنا بتمييز اسم العلامة المرجعية في Microsoft Word عبر إدراج -> روابط -> علامة مرجعية، وضغطنا على "انتقال إلى",
// سوف يقفز المؤشر إلى النص المحاط بين عقدتي BookmarkStart وBookmarkEnd.
builder->StartBookmark(u"My Bookmark");
builder->Write(u"Contents of MyBookmark.");
builder->EndBookmark(u"My Bookmark");

// يتم تخزين العلامات المرجعية في هذه المجموعة.
ASSERT_EQ(u"My Bookmark", doc->get_Range()->get_Bookmarks()->idx_get(0)->get_Name());

doc->Save(get_ArtifactsDir() + u"Bookmarks.Insert.docx");
```

## انظر أيضًا

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
