---
title: "Aspose::Words::Saving::BookmarksOutlineLevelCollection class"
linktitle: "BookmarksOutlineLevelCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::BookmarksOutlineLevelCollection class. مجموعة من مستويات مخطط العلامات المرجعية الفردية. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class


مجموعة من مستويات مخطط العلامات المرجعية الفردية. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/).

```cpp
class BookmarksOutlineLevelCollection : public System::Collections::Generic::IEnumerable<System::Collections::Generic::KeyValuePair<System::String, int32_t>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(const System::String\&, int32_t) | يضيف علامة مرجعية إلى المجموعة. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [BookmarksOutlineLevelCollection](./bookmarksoutlinelevelcollection/)() |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](./contains/)(const System::String\&) | يحدد ما إذا كانت المجموعة تحتوي على علامة مرجعية بالاسم المحدد. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | يحصل أو يضبط مستوى مخطط العلامة المرجعية بناءً على اسم العلامة المرجعية. |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يضبط مستوى مخطط العلامة المرجعية عند الفهرس المحدد. |
| [idx_set](./idx_set/)(const System::String\&, int32_t) | يحصل أو يضبط مستوى مخطط العلامة المرجعية بناءً على اسم العلامة المرجعية. |
| [idx_set](./idx_set/)(int32_t, int32_t) | يحصل أو يضبط مستوى مخطط العلامة المرجعية عند الفهرس المحدد. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | يرجع الفهرس الصفري للعلامة المرجعية المحددة في المجموعة. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | يزيل علامة مرجعية بالاسم المحدد من المجموعة. |
| [RemoveAt](./removeat/)(int32_t) | يزيل علامة مرجعية في الفهرس المحدد. |
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


المفتاح هو اسم علامة مرجعية كسلسلة غير حساسة لحالة الأحرف. القيمة هي مستوى مخطط العلامة المرجعية كعدد صحيح.

[Bookmark](../../aspose.words/bookmark/) outline level may be a value from 0 to 9. Specify 0 and Word bookmark will not be displayed in the document outline. Specify 1 and Word bookmark will be displayed in the document outline at level 1; 2 for level 2 and so on.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
