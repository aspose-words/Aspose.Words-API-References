---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.BookmarksOutlineLevelCollection—أداة قوية لإدارة الإشارات المرجعية وتحسين التنقل في المستندات بسهولة.
type: docs
weight: 5590
url: /ar/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

مجموعة من العلامات المرجعية الفردية على مستوى المخطط التفصيلي.

لمعرفة المزيد، قم بزيارة[العمل مع الإشارات المرجعية](https://docs.aspose.com/words/net/working-with-bookmarks/) مقالة توثيقية.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | يحصل على أو يعين مستوى مخطط الإشارة المرجعية حسب اسم الإشارة المرجعية. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | يضيف إشارة مرجعية إلى المجموعة. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | يحدد ما إذا كانت المجموعة تحتوي على إشارة مرجعية بالاسم المحدد. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | يعيد الفهرس المبني على الصفر للإشارة المرجعية المحددة في المجموعة. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | يزيل إشارة مرجعية بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | يزيل الإشارة المرجعية في الفهرس المحدد. |

## ملاحظات

المفتاح هو اسم إشارة مرجعية لسلسلة لا تراعي حالة الأحرف. القيمة هي مستوى مخطط إشارة مرجعية من نوع int.

قد يكون مستوى مخطط الإشارة المرجعية قيمة من 0 إلى 9. حدد 0 ولن يتم عرض الإشارة المرجعية لـ Word في مخطط المستند. حدد 1 وسيتم عرض الإشارة المرجعية لـ Word في مخطط المستند في المستوى 1؛ 2 للمستوى 2 وهكذا.

## أمثلة

يوضح كيفية تعيين مستويات الخطوط العريضة للإشارات المرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج إشارة مرجعية مع وجود إشارة مرجعية أخرى متداخلة بداخلها.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

//إدراج إشارة مرجعية أخرى.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// عند الحفظ بصيغة .pdf، يمكن الوصول إلى الإشارات المرجعية عبر قائمة منسدلة واستخدامها كمرسيات من قبل معظم القراء.
// يمكن أن تحتوي الإشارات المرجعية أيضًا على قيم رقمية لمستويات المخطط التفصيلي،
// تمكين إدخالات المخطط التفصيلي ذات المستوى الأدنى لإخفاء إدخالات الطفل ذات المستوى الأعلى عند طيها في القارئ.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// يمكننا إزالة عنصرين بحيث يتبقى فقط تعيين مستوى المخطط التفصيلي لـ "الإشارة المرجعية 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// هناك تسعة مستويات للمخطط. سيتم تحسين ترقيمها أثناء عملية الحفظ.
// في هذه الحالة، سوف تصبح المستويات "5" و"9" "2" و"3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// سيؤدي إفراغ هذه المجموعة إلى الحفاظ على الإشارات المرجعية ووضعها جميعًا على نفس مستوى المخطط التفصيلي.
outlineLevels.Clear();
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
