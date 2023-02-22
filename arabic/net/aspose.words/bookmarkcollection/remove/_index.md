---
title: BookmarkCollection.Remove
second_title: Aspose.Words لمراجع .NET API
description: BookmarkCollection طريقة. يزيل الإشارة المرجعية المحددة من المستند.
type: docs
weight: 50
url: /ar/net/aspose.words/bookmarkcollection/remove/
---
## Remove(Bookmark) {#remove}

يزيل الإشارة المرجعية المحددة من المستند.

```csharp
public void Remove(Bookmark bookmark)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmark | Bookmark | المرجعية المراد إزالتها. |

### أمثلة

يوضح كيفية إزالة الإشارات المرجعية من مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل خمس إشارات مرجعية مع نص داخل حدودها.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// هذه المجموعة تخزن الإشارات المرجعية.
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

// 3 - إزالة إشارة مرجعية من المجموعة بالاسم:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - إزالة إشارة مرجعية من فهرس في مجموعة الإشارات المرجعية:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// يمكننا مسح مجموعة الإشارات المرجعية بأكملها.
bookmarks.Clear();

// لا يزال النص الموجود داخل الإشارات المرجعية موجودًا في المستند.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Bookmark](../../bookmark/)
* class [BookmarkCollection](../)
* مساحة الاسم [Aspose.Words](../../bookmarkcollection/)
* المجسم [Aspose.Words](../../../)

---

## Remove(string) {#remove_1}

يزيل إشارة مرجعية بالاسم المحدد.

```csharp
public void Remove(string bookmarkName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| bookmarkName | String | الاسم غير الحساس لحالة الأحرف للإشارة المرجعية المراد إزالتها. |

### أمثلة

يوضح كيفية إزالة الإشارات المرجعية من مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل خمس إشارات مرجعية مع نص داخل حدودها.
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// هذه المجموعة تخزن الإشارات المرجعية.
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

// 3 - إزالة إشارة مرجعية من المجموعة بالاسم:
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - إزالة إشارة مرجعية من فهرس في مجموعة الإشارات المرجعية:
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// يمكننا مسح مجموعة الإشارات المرجعية بأكملها.
bookmarks.Clear();

// لا يزال النص الموجود داخل الإشارات المرجعية موجودًا في المستند.
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### أنظر أيضا

* class [BookmarkCollection](../)
* مساحة الاسم [Aspose.Words](../../bookmarkcollection/)
* المجسم [Aspose.Words](../../../)


