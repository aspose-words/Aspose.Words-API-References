---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt طريقة"
linktitle: "RemoveAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt طريقة. يزيل إشارة مرجعية عند الفهرس المحدد في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/removeat/
---
## BookmarksOutlineLevelCollection::RemoveAt method


يزيل علامة مرجعية في الفهرس المحدد.

```cpp
void Aspose::Words::Saving::BookmarksOutlineLevelCollection::RemoveAt(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري. |

## أمثلة



يعرض كيفية ضبط مستويات المخطط للعلامات المرجعية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدخل علامة مرجعية مع علامة مرجعية أخرى متداخلة بداخلها.
builder->StartBookmark(u"Bookmark 1");
builder->Writeln(u"Text inside Bookmark 1.");

builder->StartBookmark(u"Bookmark 2");
builder->Writeln(u"Text inside Bookmark 1 and 2.");
builder->EndBookmark(u"Bookmark 2");

builder->Writeln(u"Text inside Bookmark 1.");
builder->EndBookmark(u"Bookmark 1");

// أدخل علامة مرجعية أخرى.
builder->StartBookmark(u"Bookmark 3");
builder->Writeln(u"Text inside Bookmark 3.");
builder->EndBookmark(u"Bookmark 3");

// عند الحفظ إلى .pdf، يمكن الوصول إلى العلامات المرجعية عبر قائمة منسدلة وتُستخدم كمرساة من قبل معظم القُرّاء.
// يمكن للعلامات المرجعية أيضًا أن تحتوي على قيم رقمية لمستويات المخطط،
// مما يتيح لإدخالات المخطط ذات المستوى الأدنى إخفاء الإدخالات الفرعية ذات المستوى الأعلى عند طيها في القارئ.
auto pdfSaveOptions = System::MakeObject<Aspose::Words::Saving::PdfSaveOptions>();
System::SharedPtr<Aspose::Words::Saving::BookmarksOutlineLevelCollection> outlineLevels = pdfSaveOptions->get_OutlineOptions()->get_BookmarksOutlineLevels();

outlineLevels->Add(u"Bookmark 1", 1);
outlineLevels->Add(u"Bookmark 2", 2);
outlineLevels->Add(u"Bookmark 3", 3);

ASSERT_EQ(3, outlineLevels->get_Count());
ASSERT_TRUE(outlineLevels->Contains(u"Bookmark 1"));
ASSERT_EQ(1, outlineLevels->idx_get(0));
ASSERT_EQ(2, outlineLevels->idx_get(u"Bookmark 2"));
ASSERT_EQ(2, outlineLevels->IndexOfKey(u"Bookmark 3"));

// يمكننا إزالة عنصرين بحيث يبقى فقط تعيين مستوى المخطط للعلامة المرجعية "Bookmark 1".
outlineLevels->RemoveAt(2);
outlineLevels->Remove(u"Bookmark 2");

// هناك تسعة مستويات مخطط. سيتم تحسين ترقيمها أثناء عملية الحفظ.
// في هذه الحالة، ستصبح المستويات "5" و "9" "2" و "3".
outlineLevels->Add(u"Bookmark 2", 5);
outlineLevels->Add(u"Bookmark 3", 9);

doc->Save(get_ArtifactsDir() + u"BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// إفراغ هذه المجموعة سيحافظ على العلامات المرجعية ويضعها جميعًا على نفس مستوى المخطط.
outlineLevels->Clear();
```

## انظر أيضًا

* Class [BookmarksOutlineLevelCollection](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
