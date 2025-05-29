---
title: BookmarkCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: 使用 BookmarkCollection Clear 方法轻松清除文档中的所有书签。立即简化您的工作流程，增强组织能力！
type: docs
weight: 30
url: /zh/net/aspose.words/bookmarkcollection/clear/
---
## BookmarkCollection.Clear method

从此收藏集和文档中删除所有书签。

```csharp
public void Clear()
```

## 例子

展示如何从文档中删除书签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入五个书签，并在其边界内添加文本。
for (int i = 1; i <= 5; i++)
{
    string bookmarkName = "MyBookmark_" + i;

    builder.StartBookmark(bookmarkName);
    builder.Write($"Text inside {bookmarkName}.");
    builder.EndBookmark(bookmarkName);
    builder.InsertBreak(BreakType.ParagraphBreak);
}

// 此集合存储书签。
BookmarkCollection bookmarks = doc.Range.Bookmarks;

Assert.AreEqual(5, bookmarks.Count);

// 有几种方法可以删除书签。
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

// 4 - 删除书签集合中某个索引处的书签：
doc.Range.Bookmarks.RemoveAt(0);

Assert.False(bookmarks.Any(b => b.Name == "MyBookmark_4"));

// 我们可以清除整个书签集合。
bookmarks.Clear();

// 书签内的文本仍然存在于文档中。
Assert.AreEqual(0, bookmarks.Count);
Assert.AreEqual("Text inside MyBookmark_1.\r" +
                "Text inside MyBookmark_2.\r" +
                "Text inside MyBookmark_3.\r" +
                "Text inside MyBookmark_4.\r" +
                "Text inside MyBookmark_5.", doc.GetText().Trim());
```

### 也可以看看

* class [BookmarkCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
