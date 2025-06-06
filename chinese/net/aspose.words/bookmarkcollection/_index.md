---
title: BookmarkCollection Class
linktitle: BookmarkCollection
articleTitle: BookmarkCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.BookmarkCollection 类，这是一个用于管理文档中的书签、增强组织和导航的强大工具。
type: docs
weight: 240
url: /zh/net/aspose.words/bookmarkcollection/
---
## BookmarkCollection class

的集合[`Bookmark`](../bookmark/)表示指定范围内的书签的对象。

要了解更多信息，请访问[使用书签](https://docs.aspose.com/words/net/working-with-bookmarks/)文档文章。

```csharp
public class BookmarkCollection : IEnumerable<Bookmark>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/bookmarkcollection/count/) { get; } | 返回收藏夹中的书签数量。 |
| [Item](../../aspose.words/bookmarkcollection/item/) { get; } | 返回指定索引处的书签。 (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words/bookmarkcollection/clear/)() | 从此收藏集和文档中删除所有书签。 |
| [GetEnumerator](../../aspose.words/bookmarkcollection/getenumerator/)() | 返回一个枚举器对象。 |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove)(*[Bookmark](../bookmark/)*) | 从文档中删除指定的书签。 |
| [Remove](../../aspose.words/bookmarkcollection/remove/#remove_1)(*string*) | 删除具有指定名称的书签。 |
| [RemoveAt](../../aspose.words/bookmarkcollection/removeat/)(*int*) | 删除指定索引处的书签。 |

## 例子

展示如何添加书签并更新其内容。

```csharp
public void CreateUpdateAndPrintBookmarks()
{
    // 创建一个包含三个书签的文档，然后使用自定义文档访问者实现来打印其内容。
    Document doc = CreateDocumentWithBookmarks(3);
    BookmarkCollection bookmarks = doc.Range.Bookmarks;
    PrintAllBookmarkInfo(bookmarks);

    // 可以通过索引或名称在书签集合中访问书签，并且可以更新其名称。
    bookmarks[0].Name = $"{bookmarks[0].Name}_NewName";
    bookmarks["MyBookmark_2"].Text = $"Updated text contents of {bookmarks[1].Name}";

    // 再次打印所有书签以查看更新的值。
    PrintAllBookmarkInfo(bookmarks);
}

/// <summary>
/// 创建具有给定数量书签的文档。
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

* class [Bookmark](../bookmark/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
