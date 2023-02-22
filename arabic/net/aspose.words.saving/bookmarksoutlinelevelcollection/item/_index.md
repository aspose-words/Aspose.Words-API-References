---
title: BookmarksOutlineLevelCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: BookmarksOutlineLevelCollection ملكية. الحصول على أو تحديد مستوى مخطط الإشارة المرجعية بواسطة اسم الإشارة المرجعية.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

الحصول على أو تحديد مستوى مخطط الإشارة المرجعية بواسطة اسم الإشارة المرجعية.

```csharp
public int this[string name] { get; set; }
```

| معامل | وصف |
| --- | --- |
| name | اسم إشارة مرجعية غير حساس لحالة الأحرف. |

### قيمة الإرجاع

مستوى المخطط التفصيلي للإشارة المرجعية. النطاق الصالح هو 0 إلى 9.

### أمثلة

يوضح كيفية تعيين مستويات المخطط التفصيلي للإشارات المرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل إشارة مرجعية مع إشارة مرجعية أخرى متداخلة بداخلها.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// أدخل إشارة مرجعية أخرى.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// عند الحفظ في .pdf ، يمكن الوصول إلى الإشارات المرجعية من خلال القائمة المنسدلة واستخدامها كإرساء من قبل معظم القراء.
// يمكن أن تحتوي الإشارات المرجعية أيضًا على قيم رقمية لمستويات المخطط التفصيلي ،
// تمكين إدخالات المخطط التفصيلي ذات المستوى الأدنى لإخفاء الإدخالات الفرعية ذات المستوى الأعلى عند طيها في القارئ.
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

// يمكننا إزالة عنصرين بحيث لا يتبقى سوى تعيين مستوى المخطط التفصيلي لـ "الإشارة المرجعية 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// هناك تسعة مستويات للمخطط التفصيلي. سيتم تحسين ترقيمهم أثناء عملية الحفظ.
// في هذه الحالة ، ستصبح المستويات "5" و "9" هي "2" و "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// سيحافظ تفريغ هذه المجموعة على الإشارات المرجعية ويضعها جميعًا في نفس مستوى المخطط التفصيلي.
outlineLevels.Clear();
```

### أنظر أيضا

* class [BookmarksOutlineLevelCollection](../)
* مساحة الاسم [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* المجسم [Aspose.Words](../../../)

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

الحصول على أو تحديد مستوى مخطط الإشارة المرجعية في الفهرس المحدد.

```csharp
public int this[int index] { get; set; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس الإشارة المرجعية على أساس الصفر. |

### قيمة الإرجاع

مستوى المخطط التفصيلي للإشارة المرجعية. النطاق الصالح هو 0 إلى 9.

### أمثلة

يوضح كيفية تعيين مستويات المخطط التفصيلي للإشارات المرجعية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل إشارة مرجعية مع إشارة مرجعية أخرى متداخلة بداخلها.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// أدخل إشارة مرجعية أخرى.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// عند الحفظ في .pdf ، يمكن الوصول إلى الإشارات المرجعية من خلال القائمة المنسدلة واستخدامها كإرساء من قبل معظم القراء.
// يمكن أن تحتوي الإشارات المرجعية أيضًا على قيم رقمية لمستويات المخطط التفصيلي ،
// تمكين إدخالات المخطط التفصيلي ذات المستوى الأدنى لإخفاء الإدخالات الفرعية ذات المستوى الأعلى عند طيها في القارئ.
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

// يمكننا إزالة عنصرين بحيث لا يتبقى سوى تعيين مستوى المخطط التفصيلي لـ "الإشارة المرجعية 1".
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// هناك تسعة مستويات للمخطط التفصيلي. سيتم تحسين ترقيمهم أثناء عملية الحفظ.
// في هذه الحالة ، ستصبح المستويات "5" و "9" هي "2" و "3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// سيحافظ تفريغ هذه المجموعة على الإشارات المرجعية ويضعها جميعًا في نفس مستوى المخطط التفصيلي.
outlineLevels.Clear();
```

### أنظر أيضا

* class [BookmarksOutlineLevelCollection](../)
* مساحة الاسم [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* المجسم [Aspose.Words](../../../)


