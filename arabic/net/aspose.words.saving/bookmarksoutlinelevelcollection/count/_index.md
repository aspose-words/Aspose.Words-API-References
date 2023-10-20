---
title: BookmarksOutlineLevelCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: BookmarksOutlineLevelCollection Count ملكية. الحصول على عدد العناصر الموجودة في المجموعة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/bookmarksoutlinelevelcollection/count/
---
## BookmarksOutlineLevelCollection.Count property

الحصول على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

## أمثلة

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

// عند الحفظ بصيغة pdf.، يمكن الوصول إلى الإشارات المرجعية عبر القائمة المنسدلة واستخدامها كنقاط ارتساء من قبل معظم القراء.
// يمكن أن تحتوي الإشارات المرجعية أيضًا على قيم رقمية لمستويات المخطط التفصيلي،
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

// هناك تسعة مستويات المخطط التفصيلي. سيتم تحسين ترقيمها أثناء عملية الحفظ.
// في هذه الحالة، سيصبح المستويان "5" و"9" "2" و"3".
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// سيؤدي إفراغ هذه المجموعة إلى الحفاظ على الإشارات المرجعية ووضعها كلها على نفس مستوى المخطط التفصيلي.
outlineLevels.Clear();
```

### أنظر أيضا

* class [BookmarksOutlineLevelCollection](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
