---
title: BookmarkCollection.Remove
second_title: Aspose.Words for .NET API 参考
description: BookmarkCollection 方法. 从文档中删除指定的书签
type: docs
weight: 50
url: /zh/net/aspose.words/bookmarkcollection/remove/
---
## Remove(Bookmark) {#remove}

从文档中删除指定的书签。

```csharp
public void Remove(Bookmark bookmark)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmark | Bookmark | 要删除的书签。 |

### 例子

显示如何从文档中删除书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在边界内插入五个带有文本的书签。
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// 这个集合存储书签。
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// 有几种删除书签的方法。
// 1 - 调用书签的 Remove 方法：
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - 将书签传递给集合的 Remove 方法：
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - 按名称从集合中删除书签：
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - 删除书签集合中索引处的书签：
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// 我们可以清除整个书签集合。
bookmarks.Clear();

// 书签中的文本仍然存在于文档中。
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### 也可以看看

* class [Bookmark](../../bookmark/)
* class [BookmarkCollection](../)
* 命名空间 [Aspose.Words](../../bookmarkcollection/)
* 部件 [Aspose.Words](../../../)

---

## Remove(string) {#remove_1}

删除具有指定名称的书签。

```csharp
public void Remove(string bookmarkName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| bookmarkName | String | 要删除的书签的不区分大小写的名称。 |

### 例子

显示如何从文档中删除书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 在边界内插入五个带有文本的书签。
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// 这个集合存储书签。
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// 有几种删除书签的方法。
// 1 - 调用书签的 Remove 方法：
bookmarks["MyBookmark_1"].Remove();

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_1"));

// 2 - 将书签传递给集合的 Remove 方法：
Bookmark bookmark = doc.Range.Bookmarks[0];
doc.Range.Bookmarks.Remove(bookmark);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_2"));

// 3 - 按名称从集合中删除书签：
doc.Range.Bookmarks.Remove("MyBookmark_3");

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_3"));

// 4 - 删除书签集合中索引处的书签：
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// 我们可以清除整个书签集合。
bookmarks.Clear();

// 书签中的文本仍然存在于文档中。
Assert.That(bookmarks, Is.Empty);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### 也可以看看

* class [BookmarkCollection](../)
* 命名空间 [Aspose.Words](../../bookmarkcollection/)
* 部件 [Aspose.Words](../../../)


