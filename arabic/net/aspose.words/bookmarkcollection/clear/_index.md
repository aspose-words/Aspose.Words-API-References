---
title: BookmarkCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words لـ .NET
description: امسح جميع الإشارات المرجعية من مستندك بسهولة باستخدام طريقة BookmarkCollection Clear. بسّط سير عملك وحسّن تنظيمك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words/bookmarkcollection/clear/
---
## BookmarkCollection.Clear method

يزيل جميع الإشارات المرجعية من هذه المجموعة ومن المستند.

```csharp
public void Clear()
```

## أمثلة

يوضح كيفية إزالة الإشارات المرجعية من المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل خمس إشارات مرجعية تحتوي على نص داخل حدودها.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

//تخزن هذه المجموعة الإشارات المرجعية.
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// هناك عدة طرق لإزالة الإشارات المرجعية.
// 1 - استدعاء طريقة إزالة الإشارة المرجعية:
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - تمرير الإشارة المرجعية إلى طريقة إزالة المجموعة:
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - إزالة إشارة مرجعية من المجموعة حسب الاسم:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - إزالة إشارة مرجعية من فهرس في مجموعة الإشارات المرجعية:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

//يمكننا مسح مجموعة الإشارات المرجعية بأكملها.
bookmarks.Clear();

// النص الذي كان داخل الإشارات المرجعية لا يزال موجودًا في المستند.
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### أنظر أيضا

* class [BookmarkCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
