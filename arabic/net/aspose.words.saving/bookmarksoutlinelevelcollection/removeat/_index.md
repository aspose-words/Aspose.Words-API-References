---
title: BookmarksOutlineLevelCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words لـ .NET
description: أدر إشاراتك المرجعية بسهولة باستخدام طريقة RemoveAt. أزل الإشارات المرجعية بسرعة حسب الفهرس لتجربة استخدام مبسطة في تطبيقك!
type: docs
weight: 100
url: /ar/net/aspose.words.saving/bookmarksoutlinelevelcollection/removeat/
---
## BookmarksOutlineLevelCollection.RemoveAt method

يزيل الإشارة المرجعية في الفهرس المحدد.

```csharp
public void RemoveAt(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | المؤشر المبني على الصفر. |

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

* class [BookmarksOutlineLevelCollection](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
