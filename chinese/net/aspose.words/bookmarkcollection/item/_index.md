---
title: Item
second_title: Aspose.Words for .NET API 参考
description: 返回指定索引处的书签
type: docs
weight: 20
url: /zh/net/aspose.words/bookmarkcollection/item/
---
## BookmarkCollection indexer (1 of 2)

返回指定索引处的书签。

```csharp
public Bookmark this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 集合中的索引。 |

### 评论

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。 例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

### 例子

展示如何添加书签和更新其内容。

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // 创建一个包含三个书签的文档，然后使用自定义文档访问者实现来打印其内容。
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // 书签集合中可以通过索引或名称访问书签，并且可以更新它们的名称。
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // 再次打印所有书签以查看更新的值。
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// 创建一个具有给定数量书签的文档。
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// 使用迭代器和访问者打印集合中每个书签的信息。
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // 获取集合中的每个书签以接受将打印其内容的访问者。
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// 将每个访问过的书签的内容打印到控制台。
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### 也可以看看

* class [Bookmark](../../bookmark)
* class [BookmarkCollection](../../bookmarkcollection)
* 命名空间 [Aspose.Words](../../bookmarkcollection)
* 部件 [Aspose.Words](../../../)

---

## BookmarkCollection indexer (2 of 2)

按名称返回书签。

```csharp
public Bookmark this[string bookmarkName] { get; }
```

| 范围 | 描述 |
| --- | --- |
| bookmarkName | 不区分大小写的书签名称。 |

### 评论

如果找不到具有指定名称的书签，则返回 null。

### 例子

展示如何添加书签和更新其内容。

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // 创建一个包含三个书签的文档，然后使用自定义文档访问者实现来打印其内容。
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;

    PrintAllBookmarkInfo(bookmarks);

    // 书签集合中可以通过索引或名称访问书签，并且可以更新它们的名称。
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // 再次打印所有书签以查看更新的值。
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// 创建一个具有给定数量书签的文档。
/// </summary>
private static Document CreateDocumentWithBookmarks(int numberOfBookmarks)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    for (int i = 1; i <= numberOfBookmarks; i++)
    {
        string bookmarkName = "MyBookmark_" + i;

        builder.Write("Text before bookmark.");
        builder.StartBookmark(bookmarkName);
        builder.Write($"Text inside {bookmarkName}.");
        builder.EndBookmark(bookmarkName);
        builder.Writeln("Text after bookmark.");
    }

    return doc;
}

/// <summary>
/// 使用迭代器和访问者打印集合中每个书签的信息。
/// </summary>
private static void PrintAllBookmarkInfo(BookmarkCollection bookmarks)
{
    BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

    // 获取集合中的每个书签以接受将打印其内容的访问者。
    using (IEnumerator<Bookmark> enumerator = bookmarks.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Bookmark currentBookmark = enumerator.Current;

            if (currentBookmark != null)
            {
                currentBookmark.BookmarkStart.Accept(bookmarkVisitor);
                currentBookmark.BookmarkEnd.Accept(bookmarkVisitor);

                Console.WriteLine(currentBookmark.BookmarkStart.GetText());
            }
        }
    }
}

/// <summary>
/// 将每个访问过的书签的内容打印到控制台。
/// </summary>
public class BookmarkInfoPrinter : DocumentVisitor
{
    public override VisitorAction VisitBookmarkStart(BookmarkStart bookmarkStart)
    {
        Console.WriteLine($"BookmarkStart name: \"{bookmarkStart.Name}\", Contents: \"{bookmarkStart.Bookmark.Text}\"");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBookmarkEnd(BookmarkEnd bookmarkEnd)
    {
        Console.WriteLine($"BookmarkEnd name: \"{bookmarkEnd.Name}\"");
        return VisitorAction.Continue;
    }
}
```

### 也可以看看

* class [Bookmark](../../bookmark)
* class [BookmarkCollection](../../bookmarkcollection)
* 命名空间 [Aspose.Words](../../bookmarkcollection)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
